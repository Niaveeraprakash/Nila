# php program
Program 2
<!DOCTYPE html>
<html>
<head>
    <title>Voting Eligibility</title>
    <style>
        body {
            font-family: Arial;
            text-align: center;
            margin-top: 50px;
        }

        form {
            width: 300px;
            margin: auto;
            padding: 20px;
            border: 1px solid black;
        }

        input {
            padding: 8px;
            margin: 10px;
        }
    </style>
</head>

<body>

<h2>Voting Eligibility Checker</h2>

<form method="post">
    Enter Age:
    <input type="number" name="age" required>
    <br>
    <input type="submit" value="Check Eligibility">
</form>

<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {

    $age = $_POST["age"];

    if ($age >= 18) {
        echo "<h3>Eligible to Vote</h3>";
    }
    else {
        echo "<h3>Not Eligible to Vote</h3>";
    }
}
?>

</body>
</html>

Output 
Voting Eligibility Checker

Enter Age: 20
[Check Eligibility]

Eligible to Vote
