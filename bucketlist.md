<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Personal Bucket List</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f7fc;
            color: #333;
        }

        header {
            background-color: #bb1177;
            color: white;
            text-align: center;
            padding: 20px 0;
        }

        header h1 {
            margin: 0;
            font-size: 2.5em;
        }

        main {
            padding: 20px;
        }

        h2 {
            text-align: center;
            color: #333;
            margin-bottom: 30px;
            text-decoration: underline; 
            text-decoration-color: #cf1f89;
        }

        ul {
            list-style-type: none;
            padding: 0;
        }

        li {
            background-color: #fff;
            margin: 10px 0;
            padding: 15px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        li .icon {
            margin-right: 15px;
            font-size: 1.5em;
        }

        li.completed {
            background-color: #d4edda;
            color: #155724;
        }

        li.completed .icon {
            color: #155724;
        }

        li .text {
            flex: 1;
        }

        li button {
            background-color: #bb1177;
            color: white;
            border: none;
            padding: 10px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1em;
            transition: background-color 0.3s ease, transform 0.3s ease; /* Smooth transition for button */
        }

        li button:hover {
            background-color:  #e46eb5;
            transform: scale(1.05); /* Slightly scale the button on hover */
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 2em;
            }

            li {
                flex-direction: column;
                text-align: center;
            }

            li button {
                width: 100%;
                margin-top: 10px;
            }
        }
    </style>
</head>
<body>

<header>
    <h1>My Personal Bucket List</h1>
</header>

<main>
    <h2>Things I Want to Do In My Life</h2>

    <ul>
        <li>
            <span class="icon">🌍</span>
            <span class="text">Travel to Germany, Japan, and New Zealand</span>
            <button onclick="markCompleted(this)">Mark as Completed</button>
        </li>
        <li>
            <span class="icon">🎢</span>
            <span class="text">Go bungee jumping</span>
            <button onclick="markCompleted(this)">Mark as Completed</button>
        </li>
        <li>
            <span class="icon">💻</span>
            <span class="text">Getting a job</span>
            <button onclick="markCompleted(this)">Mark as Completed</button>
        </li>
        <li>
            <span class="icon">❤️</span>
            <span class="text">See my parents and loved ones happy</span>
            <button onclick="markCompleted(this)">Mark as Completed</button>
        </li>
        <li>
            <span class="icon">📚</span>
            <span class="text">Read many books</span>
            <button onclick="markCompleted(this)">Mark as Completed</button>
        </li>
    </ul>
</main>

<script>
    function markCompleted(button) {
        const listItem = button.parentElement;
        listItem.classList.toggle('completed');
        button.innerText = listItem.classList.contains('completed') ? 'Undo' : 'Mark as Completed';
    }
</script>

</body>
</html>
