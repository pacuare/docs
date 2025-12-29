Query Tool
##########

*This requires you to be signed in.*

.. raw:: html

   <meta name="htmx-config" content='{"selfRequestsOnly": false}' />
   <script src="https://cdn.jsdelivr.net/npm/htmx.org@2.0.8/dist/htmx.min.js"></script>
   <script src="https://unpkg.com/htmx-ext-form-json"></script>
   <div style="display: flex; flex-direction: column; align-items: stretch; gap: 5px;">
       <form style="display: flex; flex-direction: column; align-items: stretch; gap: 5px;"
               hx-target="#query-result"
               hx-swap="innerHTML"
               hx-post="https://api.pacuare.dev/v1/query.html"
               hx-ext="form-json"
               hx-request='{"credentials":true}'>
           <textarea name="query"></textarea>
           <button type="Submit" style="display: block">Query</button>
       </form>
       <div id="query-result" style="overflow:auto; max-height: 75vh;"></div>
   </div>
   <script>
    document.addEventListener('htmx:load', () => {
        const table = document.querySelector('#query-result table')
        table.classList.add('docutils')
        table.classList.add('align-default')
    })
   </script>
