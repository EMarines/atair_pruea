<script>
  import { Router, Route, Link } from "svelte-navigator";
   import Home from './Home.svelte'
   import Contactos from './Contactos.svelte'
   import Propiedades from './Propiedades.svelte'
   import Captacion from './Captacion.svelte'
   import Agenda from './Agenda.svelte'   
   import About from './About.svelte'
   import logoMH from '../assets/logoMH.png'
   

  
  </script>
  
  <nav class="navbar navbar-expand-lg navbar-light">
      <div class="container-fluid">
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarTogglerDemo03" aria-controls="navbarTogglerDemo03" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <a class="navbar-brand" href="https://matchhome.net">MatchHome</a>
        <div class="collapse navbar-collapse" id="navbarTogglerDemo03">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <Router>
              <div class="navMenu">
              <ul>
                <li class= "active">
                  <Link to="/">Home</Link>
                </li>
                <li class="hide">
                  <Link to="contactos">Contactos</Link>
                </li>
                <li>
                  <Link to="propiedades">Propiedades</Link>
                </li>
                <li>
                  <Link to="captacion">Captación</Link>            
                </li>
                <li>
                  <Link to="agenda">Agenda</Link>
                </li>
                <li>
                  <Link to="about">About</Link>
                </li>
      
              </ul>
              </div>
              
              <main>
                <Route path="/">
                  <Home />
                </Route>
                
                <Route path="contactos">
                  <Contactos />
                </Route>
                
                <Route path="propiedades">
                  <Propiedades />
                </Route>
                
                <Route path="captacion">
                  <Captacion />
                </Route>
                
                <Route path="agenda">
                  <Agenda />
                </Route>
                
                <Route path="about">
                  <About />
                </Route>
                
              </main>
      
              
            <a href="https://matchhome.net" target="_blank" class="enlace"> 
              <img src={logoMH} class="logoMH" alt="MatchHome" />
            </a>
              
            </Router>
            </ul>
  
  
            <!-- {#if firebase.auth = true} -->
              <form class="d-flex">
                <input class="form-control me-2" type="search" placeholder="Buscar" aria-label="Search">
                <button class="btn btn-outline-success" type="submit">Contacto o Propiedad</button>
              </form>
            <!-- {/if} -->
        </div>
      </div>
    </nav>
  
  