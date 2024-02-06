# delete-column-in-data-tables
delete column in data table from click button print when click print button then its delete column first set in script  code data table id and secondly which specific column dleete set index number 

this si a button which doin print work 
<button id="printButton" class="btn btn-outline-primary ms-3 fw-bolder" ><i
                  class="i-Add me-2 font-weight-bold"></i>Print</button>


and this is script code in this script code first set iin table id and secondly whcich specific column dlete index number set 

<script>
    document.getElementById("printButton").addEventListener("click", function() {
          var table = document.getElementById("purchase_table");
          if (table) {
              // Clone the table
              var tableClone = table.cloneNode(true);
  
              // Exclude the "image" column
          //     Array.from(tableClone.rows).forEach(function(row) {
          //     row.deleteCell(8); // Remove the first column
  
          // });
              
              var newWin = window.open('', 'Print-Window');
              newWin.document.open();
              newWin.document.write('<html><head><link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css"></head><body>' +           tableClone.outerHTML + '</body></html>');
              newWin.document.close();
              setTimeout(function() {
                  newWin.print();
                  newWin.close();
              }, 10);
          }
      });
  
    </script>
