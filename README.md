# js_add_generating_html_with_button
 
```html
<!DOCTYPE html>
<html>
  <!-- https://www.geeksforgeeks.org/how-to-append-html-code-to-a-div-using-javascript/ -->

  <head>
    <title>How to Append HTML Code to a Div using Javascript</title>
  </head>

  <body>
    <div id="add_to_me"></div>

    <button onclick="addCode()">Add Stuff</button>

    <input type="submit" value="ADD" id='addButton'>
    <div id="new"></div>

    <script>
      function addCode() {
        document.getElementById("add_to_me").innerHTML +=
          "<h3>This is the text which has been inserted by JS</h3>";
      }
      document.getElementById('addButton')
        .onclick = function () {
          pDiv = document.getElementById('new');
          var n = pDiv.childNodes.length + 1;
          var newDiv = document.createElement("div");
          newDiv.innerHTML = n + '. Question: <br /><textarea name="question' + n + '" rows="4" cols="50"></textarea><br />';
          pDiv.appendChild(newDiv);
        };
    </script>
  </body>

</html>
```
