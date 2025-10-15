<!DOCTYPE html>
<html>
<head>
  <title>Students</title>
</head>
<body>
  <h2>Student List</h2>
  <ul>
    {% for s in students %}
      <li>{{ s[1] }} - Grade: {{ s[2] }}</li>
    {% endfor %}
  </ul>

  <h3>Add New Student</h3>
  <form method="post" action="{{ url_for('add_student') }}">
    <input type="text" name="name" placeholder="Name" required>
    <input type="text" name="grade" placeholder="Grade" required>
    <button type="submit">Add</button>
  </form>
</body>
</html>
