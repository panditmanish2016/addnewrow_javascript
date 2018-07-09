<!DOCTYPE html>
<html>
    <head>
        <title>Javascript - Add HTML Table Row </title>
        <meta charset="windows-1252">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <script>
            
            function addRow()
            {
                // get input values
                var fname = document.getElementById('fname').value;
                 var lname = document.getElementById('lname').value;
                  var age = document.getElementById('age').value;
                  
                  // get the html table
                  // 0 = the first table
                  var table = document.getElementsByTagName('table')[0];
                  
                  // add new empty row to the table
                  // 0 = in the top 
                  // table.rows.length = the end
                  // table.rows.length/2+1 = the center
                  var newRow = table.insertRow(table.rows.length/2+1);
                  
                  // add cells to the row
                  var cel1 = newRow.insertCell(0);
                  var cel2 = newRow.insertCell(1);
                  var cel3 = newRow.insertCell(2);
                  
                  // add values to the cells
                  cel1.innerHTML = fname;
                  cel2.innerHTML = lname;
                  cel3.innerHTML = age;
            }
        </script>
    </head>
    <body>
        First Name: <input type="text" name="fname" id="fname" /><br/><br/>
        Last Name: <input type="text" name="lname" id="lname" /><br/><br/>
        Age: <input type="text" name="age" id="age" /><br/><br/>
        <button onclick="addRow();">Submit</button><br/><br/>
        <table>
            <tr>
                <th>First Name</th>
                <th>Last Name</th>
                <th>Age</th>
            </tr>
            <tr>
                <td></td>
                <td></td>
                <td></td>
            </tr>
        </table>
    </body>
</html>
