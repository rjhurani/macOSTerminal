<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Directory Listing</title>
</head>
<body>
  <h1>Files in Current Directory:</h1>
  <ul>
    <?php
      $files = scandir('.');
      foreach ($files as $file) {
        if ($file !== '.' && $file !== '..') {
          echo "<li><a href='$file'>$file</a></li>";
        }
      }
    ?>
  </ul>
</body>
</html>
