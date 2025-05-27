Useful SQL Queries
******************

There are a few common queries you might want to know in order to work with the database; a few of them are listed here, in no particular order.

``unique_turtles``
==================


This view allows you to see all of the individual turtles that have been seen, along with all of the injuries that have been recorded for each turtle.

.. code-block:: sql
   
   CREATE VIEW unique_turtles AS
	   SELECT
	   	count(turtle_id) AS turtle_occurrences,
	   	string_agg(injuries, ''::text) AS injuries
	   FROM pacuare_raw
	   WHERE (turtle_id <> ''::text)
	   GROUP BY turtle_id;
   
``spanish_bool``
================

The ``pacuare_raw`` table is `raw` data. This means that there are a few quirks --
one being that booleans, instead of being ``true`` or ``false``, are ``SI`` or ``NO``.
To turn these into booleans, you can use this function.

.. code-block:: sql
   
   CREATE OR REPLACE FUNCTION public.spanish_bool(str_val text)
   RETURNS boolean 
   LANGUAGE plpgsql
   AS $$ BEGIN
   	IF lower(str_val) = 'si' THEN
   		RETURN TRUE;
   	ELSE
   		RETURN FALSE;
   	END IF;
   END $$;