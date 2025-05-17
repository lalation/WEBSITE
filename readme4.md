<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Madoka Magica</title>
    <link rel="stylesheet" href="style.css">
    <script src="https://kit.fontawesome.com/b4761de563.js" crossorigin="anonymous"></script>
 <head>
<body style="background-color:  rgb(246, 238, 255); background-image: url(https://i.postimg.cc/fyrZ4vwr/purple-removebg-preview.png); background-repeat: repeat; background-size: 5%;"></body>

    <div id="header">
    <div class="container">
        <nav>
      <ul id="sidemenu">
                <li><a style="color: rgb(9, 0, 12);" href="Home.html">Home</a></li>
                <li><a style="color: rgb(9, 0, 12);"  href="About Us.html">About Us</a></li>
                <li><a style="color: rgb(9, 0, 12);" href="Projects.html">Projects</a></li>
                <li><a style="color: rgb(9, 0, 12);" href="Contact Us.html">Contact Us</a></li>
                <i class="fa-solid fa-circle-xmark" onclick="closemenu()"></i>
            </ul>
            <i class="fa-solid fa-bars" onclick="openmenu()"></i>
            </nav>
     <div class="contact">
    <div class="container">
        <div class="row">
            <div class="contact-left">
                <h1 class="sub-title" style="font-size: 80px; text-align: center; color: rgb(38, 2, 59);">Contact Me</h1>
                <p style="font-size: 40px; text-align: center; color: rgb(9, 0, 12); font-style: oblique ;"><i class="fa-solid fa-envelope"></i>0laitan.soetan0@gmail.com</p>
                <p style="font-size: 40px; text-align: center; color: rgb(9, 0, 12); font-style: oblique;"><i class="fa-solid fa-phone"></i> 09090405375</p>
                <div class="social-icons">
                    <a href="https://web.facebook.com/?_rdc=1&_rdr"><i class="fa-brands fa-facebook"></i> </a>
                     <a href="https://www.instagram.com/"><i class="fa-brands fa-square-instagram"></i> </a>
                      <a href="https://www.linkedin.com/"><i class="fa-brands fa-linkedin"></i> </a>
                </div>
             </div>   
                <div class="contact-right">
                    <form name="submit-to-google-sheet">
                        <input type="text" name="Name" placeholder="Your Name" required>
                        <input type="email" name="Email" placeholder="Your Email" required>
                        <textarea name="Message" rows="6" placeholder="Your Message"></textarea>
                        <button type="submit" class="btn">Submit</button>
                    </form>
                    <span id="msg"></span>



                </div>
            </div>
        </div>
    </div>
    <div class="copyright">
        <p> Copyright @ Olaitan. <i class="fa-solid fa-heart"></i> Made with GreatStack </p>
    </div>
  </div>

  <script>

    var sidemenu = document.getElementById("sidemenu");

    function openmenu(){
        sidemenu.style.right = "0"; 

    }
     function closemenu(){
        sidemenu.style.right = "-200px"; 
    }
</script>

  <script>
  const scriptURL = 'https://script.google.com/macros/s/AKfycbxh2PGRRrqyETs2OqbRvgSWmXOe1pwozGi-82yJ_T3U6kzvuHMXGKn-7vm95Lv2Cufg/exec'
  const form = document.forms['submit-to-google-sheet']
  const msg = document.getElementById("msg")

  form.addEventListener('submit', e => {
    e.preventDefault()
    fetch(scriptURL, { method: 'POST', body: new FormData(form)})
      .then(response => {
        msg.innerHTML = "Message sent Succefully"
        setTimeout(function(){
            msg.innerHTML = ""
        },5000)
        form.reset()
      })
      .catch(error => console.error('Error!', error.message))
  })
</script>
</body>
</html>
