# phppractical
<!DOCTYPE html>
<html>

<body>

    <form method="post">
        Enter 5 values:<br><br>

        <input type="number" name="values[]" required><br>
        <input type="number" name="values[]" required><br>
        <input type="number" name="values[]" required><br>
        <input type="number" name="values[]" required><br>
        <input type="number" name="values[]" required><br><br>

        <input type="submit" value="Submit">
    </form>

    <?php
    if ($_SERVER["REQUEST_METHOD"] == "POST") {
        $values = $_POST['values'];

        echo "The five values are:<br>";

        foreach ($values as $value) {
            echo $value . "<br>";
        }
    }
    ?>

</body>

</html>
