<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nos Chouchous</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f9f9f9;
            color: #333;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #ffccd5;
            padding: 20px;
            text-align: center;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        header img {
            height: 50px;
            margin-right: 10px;
        }
        main {
            padding: 20px;
        }
        .definition {
            background-color: #cce7ff;
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 20px;
        }
        .manager-section {
            display: flex;
            justify-content: space-around;
            margin-bottom: 20px;
        }
        .manager {
            text-align: center;
        }
        .manager img {
            border-radius: 50%;
            width: 100px;
            height: 100px;
            object-fit: cover;
        }
        .manager h3 {
            margin-top: 10px;
        }
        .favorite-button {
            background-color: #ffb3c1;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 10px;
        }
        .popup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            z-index: 1000;
        }
        .popup.show {
            display: block;
        }
        .popup-content {
            max-height: 300px;
            overflow-y: auto;
        }
        .popup-close {
            background: none;
            border: none;
            font-size: 16px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <header>
        <img src="https://www.fr-dba.com/wp-content/uploads/2020/11/logo-dba-vf-1.png" alt="Logo DBA">
        <h1>Nos Chouchous</h1>
    </header>
    <main>
        <div class="definition">
            <h2>Définition de Chouchou</h2>
            <p>Un chouchou est une personne ou une chose qui est particulièrement appréciée ou préférée par quelqu'un. Ce terme affectueux est souvent utilisé pour désigner les favoris dans divers contextes.</p>
        </div>
        <div class="manager-section">
            <div class="manager">
                <img src="https://media.licdn.com/dms/image/v2/C4D03AQGsE6Fv_OQmMQ/profile-displayphoto-shrink_800_800/profile-displayphoto-shrink_800_800/0/1540125746107?e=1748476800&v=beta&t=oybW8-m8CFChiyNwlpdVnNWnzUaMttJo8fjK3yPCyvo" alt="Manager Benoit">
                <h3>Benoit</h3>
                <button class="favorite-button" onclick="togglePopup('benoit')">Voir les Chouchous</button>
            </div>
            <div class="manager">
                <img src="https://media.licdn.com/dms/image/v2/C4D03AQEISt7mKRzUdQ/profile-displayphoto-shrink_800_800/profile-displayphoto-shrink_800_800/0/1539187124432?e=1748476800&v=beta&t=Z6mPEZe7DRpRB2T7XeP1Au1imwfzUxnduba_AE26YqM" alt="Manager Dan">
                <h3>Dan</h3>
                <button class="favorite-button" onclick="togglePopup('dan')">Voir les Chouchous</button>
            </div>
        </div>
        <div class="popup" id="popup-benoit">
            <div class="popup-content">
                <h3>Chouchous de Benoit</h3>
                <p>Chouchou 1 de Benoit: Description du chouchou 1 de Benoit.</p>
                <p>Chouchou 2 de Benoit: Description du chouchou 2 de Benoit.</p>
            </div>
            <button class="popup-close" onclick="togglePopup('benoit')">Fermer</button>
        </div>
        <div class="popup" id="popup-dan">
            <div class="popup-content">
                <h3>Chouchous de Dan</h3>
                <p>Chouchou 1 de Dan: Description du chouchou 1 de Dan.</p>
                <p>Chouchou 2 de Dan: Description du chouchou 2 de Dan.</p>
            </div>
            <button class="popup-close" onclick="togglePopup('dan')">Fermer</button>
        </div>
    </main>
    <script>
        function togglePopup(manager) {
            const popup = document.getElementById('popup-' + manager);
            popup.classList.toggle('show');
        }
    </script>
</body>
</html>
