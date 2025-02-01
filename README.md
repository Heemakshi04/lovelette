<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine?</title>
    <style>
        body {
            font-family: Verdana, sans-serif;
            text-align: center;
            background-color: rgba(240, 203, 226, 0.945);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            position: relative;
            overflow: hidden;
        }
        h1 {
            color: rgb(222, 88, 88);
        }
        .gif-container {
            margin-bottom: 20px;
        }
        
        .btn {
            font-size: 20px;
            padding: 10px 20px;
            cursor: pointer;
            border: none;
            border-radius: 7px;
            transition: 0.3s;
        }
        #yes {
            background-color: rgb(56, 203, 216);
        }
        #no {
            background-color: lightcoral;
            position: absolute;
        }
        /* Heart Animation */
        .heart {
            position: absolute;
            color: rgb(255, 111, 111);
            font-size: 25px;
            animation: fly 2s linear infinite;
        }
        @keyframes fly {
            0% {
                transform: translateY(0) scale(1);
                opacity: 1;
            }
            100% {
                transform: translateY(-500px) scale(0);
                opacity: 0;
            }
        }
    </style>
</head>
<body>
    <h1>Will You Be My Valentine? 💖</h1>
    
    <!-- Cute Valentine GIF -->
    <div class="gif-container">
        <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExcjljczVsNG95a29teDk3cGhvcW1uYXd5NHo5YzVraWI4cTZhM3VjYiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/8Fxae36AvVFSpgOTFO/giphy.gif" 
             alt="Cute Valentine GIF" width="300">
    </div>

    <!-- Buttons next to each other -->
    <div class="btn-container">
        <button id="yes" class="btn">Yes</button>
        <button id="no" class="btn">No</button>
    </div>

    <script>
        let noButton = document.getElementById("no");

        document.getElementById("yes").addEventListener("click", function() {
            alert("YIPEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEEE!!!!!!!! ❤️ I love you my baby <33!");
            createhearts();
            });

        document.getElementById("no").addEventListener("mouseover", function() {
            let x = Math.random() * window.innerWidth * 0.8;
            let y = Math.random() * window.innerHeight * 0.8;
            this.style.left = x + "px";
            this.style.top = y + "px";
        });

        // Function to create floating hearts
        function createhearts() {
            for (let i = 0; i < 20; i++) { // Number of hearts
                let heart = document.createElement("div");
                heart.innerHTML = "❤️";
                heart.classList.add("heart");
                document.body.appendChild(heart);

                // Randomize position
                heart.style.left = Math.random() * window.innerWidth + "px";
                heart.style.bottom = "0px";

                // Randomize animation duration
                heart.style.animationDuration = (Math.random() * 2 + 1) + "s";

                // Remove heart after animation
                setTimeout(() => {
                    heart.remove();
                }, 2000);
            }
        }
    </script>
</body>
</html>

