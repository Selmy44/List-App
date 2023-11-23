# List-App
This a List App web
<!DOCTYPE html>
<html>
<head>
  <title>List App</title>
  <style>
    /* Inline CSS for simplicity */
    body {
      font-family: Arial, sans-serif;
    }
  </style>
</head>
<body>

  <h1>List App</h1>

  <input type="text" id="listInput" placeholder="Add new item">
  <button onclick="addItem()">Add</button>

  <ul id="itemList">
    <!-- Items will be added here -->
  </ul>

  <script>
    function addItem() {
      var input = document.getElementById("listInput");
      var item = input.value;
      
      if (item === "") {
        alert("Please enter an item");
        return;
      }
      
      var itemList = document.getElementById("itemList");
      var li = document.createElement("li");
      li.appendChild(document.createTextNode(item));
      itemList.appendChild(li);
      
      input.value = ""; // Clear input field after adding item
    }
  </script>

</body>
</html>
