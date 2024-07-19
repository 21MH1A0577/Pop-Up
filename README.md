# Pop-Up
When we submitting the form then its show a pop up msg.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pop Up</title>
    <style>
        *{
            margin: 0;
            padding: 0;
            font-family: times;
            box-sizing: border-box;
        }
        .container{
            background:linear-gradient(160deg , yellow,blue) ;
            width: 100%;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .b1{
            padding: 10px 50px;
            border-radius: 25px;
            border: 2px inset orange;
            font-size: 15px;
            font-weight: 600;
            cursor: pointer;
            outline: none;
            border: 0;
        }
        .popup button{
            cursor: pointer;
            font-size: 15px;
            font-weight: 600;
            padding:10px;
            border-radius: 25px;
            width: 100%;
            background-color: #6fd649;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
        .popup{
            width: 400px;
            background: #fff;
            position: absolute;
            border-radius: 16px;
            top: 0;
            left: 50%;
            transform: translate(-50%,-50%) scale(0.1);
            text-align: center;
            color: #333;
            padding: 30px 30px 30px;
            visibility: hidden;
            transition: transform 0.4s,top 0.4s ;
        }
        .popup img{
            width: 100px;
            margin-top: -70px;
            border-radius: 50%;
            box-shadow: 0 2px 5px rgb(0,0,0,0.2);
        }
        h2{
            font-size: 38px;
            font-weight: 500px;
            margin: 30px 0 10px;

        }
        .openPopup{
            visibility: visible;
            top: 50%;
            transform: translate(-50%,-50%) scale(1);
        }
        
    </style>
</head>
<body>
    <div class="container">
        <button type="submit" class="b1" onclick="openPopup()">Submit</button>
        <div class="popup" id="popup">
            <img src="tick.jpeg">
            <h2>Thank You</h2>
            <p>Your details has been successfully submitted.Thanks!</p>
            <button type="button" onclick="closePopup()" >OK</button>
        </div>
    </div>
    <script>
        let popup=document.getElementById('popup');
        function openPopup(){
            popup.classList.add('openPopup');
        }
        function closePopup(){
            popup.classList.remove('openPopup');
        }
    </script>
</body>
</html>
