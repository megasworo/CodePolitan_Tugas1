<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Tugas 1 CodePolitan</title>
        <link rel="stylesheet" href="./css/nav.css">
        <link rel="stylesheet" href="./css/main.css">
    </head>
    <body>
        <nav class="navBar">
            <div class="navLogo">
                <a href="#Beranda">
                    <img src="./assets/logo.jpg" alt="Dough Station">
                </a>
            </div>
            <input id="menu-toggle" type="checkbox" />
            <label class='menu-button-container' for="menu-toggle">
                <div class='menu-button'></div>
            </label>
            <ul class="menu">
                <li><a href="#Beranda">Beranda</a></li>
                <li><a href="#Produk_Kami">Produk Kami</a></li>
                <li><a href="#Gallery">Gallery</a></li>
                <li><a href="#Hubungi_Kami">Hubungi Kami</a></li>
            </ul>
        </nav>
        <main>
            <div class="title">
                <h1 class="title1">Produk Kami</h1>
                <h4 class="title 2">Teman kamu menjalani hari</h4>
            </div>
            <div class="galeriProduk">
                <div class="cardProduk" onclick="openModal();currentSlide(1)">
                    <div class="imgProduk">
                        <img src="./assets/eggtart.jpg" alt="Egg Tart">
                    </div>
                    <div class="caption">
                        <h5 class="namaProduk">Egg Tart</h5>
                        <p class="harga">Rp 65,000</p>
                        <hr>
                        <button>Beli</button>
                    </div>
                </div>
                <div class="cardProduk" onclick="openModal();currentSlide(2)">
                    <div class="imgProduk">
                        <img src="./assets/ayam.jpg" alt="Chicken Wing">
                    </div>
                    <div class="caption">
                        <h5 class="namaProduk">Chicken Wing</h5>
                        <p class="harga">Rp 35,000</p>
                        <hr>
                        <button>Beli</button>
                    </div>
                </div>
                <div class="cardProduk" onclick="openModal();currentSlide(3)">
                    <div class="imgProduk">
                        <img src="./assets/apple pie.jpg" alt="Apple Pie">
                    </div>
                    <div class="caption">
                        <h5 class="namaProduk">Apple Pie</h5>
                        <p class="harga">Rp 110,000</p>
                        <hr>
                        <button>Beli</button>
                    </div>
                </div>
                <div class="cardProduk" onclick="openModal();currentSlide(4)">
                    <div class="imgProduk">
                        <img src="./assets/jamur krispi.jpg" alt="Jamur Krispi">
                    </div>
                    <div class="caption">
                        <h5 class="namaProduk">Jamur Krispi</h5>
                        <p class="harga">Rp 20,000</p>
                        <hr>
                        <button>Beli</button>
                    </div>
                </div>
                <div class="cardProduk" onclick="openModal();currentSlide(5)">
                    <div class="imgProduk">
                        <img src="./assets/zuppa.jpg" alt="Zuppa Sup">
                    </div>
                    <div class="caption">
                        <h5 class="namaProduk">Zuppa Sup</h5>
                        <p class="harga">Rp 35,000</p>
                        <hr>
                        <button>Beli</button>
                    </div>
                </div>
                <div class="cardProduk" onclick="openModal();currentSlide(6)">
                    <div class="imgProduk">
                        <img src="./assets/kopi.jpg" alt="Kopi Susu Aren">
                    </div>
                    <div class="caption">
                        <h5 class="namaProduk">Kopi Susu Gula Aren</h5>
                        <p class="harga">Rp 15,000</p>
                        <hr>
                        <button>Beli</button>
                    </div>
                </div>
            </div>
        </main>

        <div id="myModal" class="modal">
            <span class="close cursor" onclick="closeModal()">&times;</span>
            <div class="modal-content">
        
            <div class="mySlides">
                <img class="gambarProduk" src="./assets/eggtart.jpg" style="width:100%" alt="Egg Tart">
            </div>
        
            <div class="mySlides">
                <img class="gambarProduk" src="./assets/ayam.jpg" style="width:100%" alt="Chicken Wing">
            </div>
        
            <div class="mySlides">
                <img class="gambarProduk" src="./assets/apple pie.jpg" style="width:100%" alt="Apple Pie">
            </div>
            
            <div class="mySlides">
                <img class="gambarProduk" src="./assets/jamur krispi.jpg" style="width:100%" alt="Jamur Krispi">
            </div>

            <div class="mySlides">
                <img class="gambarProduk" src="./assets/zuppa.jpg" style="width:100%" alt="Zuppa Sup">
            </div>

            <div class="mySlides">
                <img class="gambarProduk" src="./assets/kopi.jpg" style="width:100%" alt="Kopi Susu Gula Aren">
            </div>
            
            <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
            <a class="next" onclick="plusSlides(1)">&#10095;</a>
        
            <div class="caption-container">
                <p id="caption"></p>
            </div>
        
            </div>
        </div>
        
        <script>
            function openModal() {
                document.getElementById("myModal").style.display = "block";
            }

            function closeModal() {
                document.getElementById("myModal").style.display = "none";
            }
            
            var slideIndex = 1;
            showSlides(slideIndex);
            
            function plusSlides(n) {
                showSlides(slideIndex += n);
            }
            
            function currentSlide(n) {
                showSlides(slideIndex = n);
            }
            
            function showSlides(n) {
                var i;
                var slides = document.getElementsByClassName("mySlides");
                var dots = document.getElementsByClassName("gambarProduk");
                var captionText = document.getElementById("caption");
                if (n > slides.length) {slideIndex = 1}
                if (n < 1) {slideIndex = slides.length}
                for (i = 0; i < slides.length; i++) {
                    slides[i].style.display = "none";
                }
                slides[slideIndex-1].style.display = "block";
                captionText.innerHTML = dots[slideIndex-1].alt;
            }
        </script>
    </body>
</html>
