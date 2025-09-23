<script>
</script>
  
<div class="sidebar">
<div class="header-container">
    <div class="bio-photo">
        <img src="/jinrui_bio.jpg" alt="bio">
    </div>
    <div class="name-container">
        <p class="name">Jinrui Wang</p>
        <p class="name-notes">Pronoun is: she/her</p>
        <p class="name-notes">Pronounced as: Gin-rey</p>
    </div>
</div>

<nav>
    <ul>
    <li><a href="#bio">Bio</a></li>
    <li><a href="#news">News</a></li>
    <li><a href="#publications">Publications</a></li>
    <li><a href="#projects">Projects</a></li>
    </ul>
</nav>

<div class="icons-container">
    <a href="https://www.linkedin.com/in/jinrui-wang/" target="_blank">
      <i class="fa-brands fa-linkedin-in"></i>
    </a>
    <a href="mailto:j.wang@ed.ac.uk">
        <i class="fa-regular fa-paper-plane"></i>
    </a>      
</div>
</div>
  

<style>
    .bio-photo {
        width: 100px; 
        height: 100px; 
        border-radius: 50%; 
        overflow: hidden; 
        float: right;
        margin: 20px 0;
      }
      
      .bio-photo img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }

    .header-container {
        display: flex;
        flex-direction: column;
        align-items: end;
    }

    .name-container {
        text-align: right;
    }

    .name {
        font-family: 'Langar';
        font-size: 1.5rem;
        /* text-align: right; */
        margin: 20px 0;
    }

    .name-notes {
        /* text-align: right; */
        margin: 0;
        padding: 0;
        font-size: 0.9em;
        line-height: 1em;
    }

    nav li {
        text-align: right;
        padding: 5px 0;
    }

    nav ul {
        list-style-type: none; 
        padding: 0;
        margin: 40px 0;
    }

    nav a {
        text-align: right;
        color: black;
        text-decoration: none;
    }


    nav a:hover {
        color: #509A23; 
        font-weight: 600;
    }

    .icons-container a {
    color: initial;
    text-decoration: none;
    }

    .icons-container a:hover {
    color: #509A23;
    }

    @media (max-width: 48rem) {
        nav {
            display: none; 
        }

        .icons-container {
            display: none; 
        }

        .bio-photo {
            width: 150px; 
            height: 150px;
        }

        .header-container {
            display: flex;
            flex-direction: row;
            align-items: center;
        }

        .name-container {
            text-align: left;
            margin-left: 3rem;
        }
    }



</style>