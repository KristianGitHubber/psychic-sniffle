# psychic-sniffle

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Christmas Calendar</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      text-align: center;
      margin: 20px;
    }

    .calendar {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 10px;
      max-width: 600px;
      margin: 0 auto;
    }

    .day {
      width: 100%;
      height: 60px;
      background-color: #e0e0e0;
      border: 1px solid #ccc;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
    }

    .day:hover {
      background-color: #d1d1d1;
    }

    .day.opened {
      background-color: #f0f0f0;
      border: 1px solid #999;
    }
  </style>
</head>
<body>

<div class="calendar">
  <!-- You can use PHP or JavaScript to dynamically generate the calendar boxes -->
  <?php for ($i = 1; $i <= 24; $i++) { ?>
    <div class="day" onclick="openDoor(<?php echo $i; ?>)"><?php echo $i; ?></div>
  <?php } ?>
</div>

<script>
  function openDoor(day) {
    var door = document.querySelector('.calendar .day:nth-child(' + day + ')');
    door.classList.add('opened');
    // You can add additional logic here, such as showing a special message or image for each day
  }
</script>

</body>
</html>
