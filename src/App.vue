<template>
<div id="app" style="position:absolute;width:100%; height:100%">

    <!-- primer contenedor -->
    <div class="contenedor" id="contenedor1">

        <!-- imagen de logo -->
        <img src="https://i.blogs.es/e79516/nuevo-logo-google/1366_2000.jpg" alt="" width="200px" style="width:200px">

        <!-- contenedor del menu  -->
        <div class="card">
            <!-- menus -->
            <div class="menu">
                <!-- icono del menu -->
                <i class="fas fa-home"></i>
                Inicio
            </div>
            <div class="menu">
                <i class="fas fa-book"></i>
                Cursos
            </div>
            <div class="menu">
                <i class="fas fa-user-graduate"></i>
                Maestros
            </div>
            <div class="menu">
                <i class="far fa-calendar-alt"></i>
                Eventos
            </div>
        </div>
        <!-- fin del contenedor del menu -->

        <!-- separador de lineas -->
        <br>

        <!-- Actualizador de cursos -->
        <div class="card chip">
            <div class="icon" style="background-color:#9C27B0;color:white">
                <i class="far fa-lightbulb"></i>
            </div>
            <div class="texto">
                Actualización de Cursos
                <div class="sub-texto">por @Walter</div>
            </div>
        </div>

        <!-- separador de lineas -->
        <br>

        <!-- Información -->
        <div id="contenedor1-abajo">
            <div id="doble">
                <div class="card chip">
                    <div class="icon" style="color:#4CAF50">
                        <i class="fas fa-medal"></i>
                    </div>
                    <div class="texto">
                        1800
                        <div class="sub-texto">Puntos</div>
                    </div>
                </div>
                <div class="card chip">
                    <div class="icon" style="color:#F44336">
                        <i class="fas fa-battery-three-quarters"></i>
                    </div>
                    <div class="texto">
                        45.3%
                        <div class="sub-texto">Completado</div>
                    </div>
                </div>
            </div>
    
            <br>

            <div class="card chip">
                <div class="imagen">
                    <img src="https://lc-imageresizer-live-s.legocdn.com/resize/ironman_slider_ironman-photo?width=1600&imageUrl=https%3A%2F%2Fwww.lego.com%2Fr%2Fwww%2Fr%2Fportals%2F-%2Fmedia%2Fcampaigns%2Fgrownup%2Fzebra%2Fironman%2F02-intro-section%2Fironman_slider_ironman-photo.jpg%3Fl.r%3D-816388879" alt="">
                </div>
                <div class="texto">
                    Programadores
                    <div class="sub-texto">@Programadores</div>
                </div>
            </div>
        </div>

        <!-- fin del contenedor 1 -->
    </div>

    <!-- contenedor 2 -->
    <div class="contenedor" id="contenedor2">

    </div>

    <!-- contenedor 3 -->
    <div class="contenedor" id="contenedor3">

    </div>
</div>
</template>

<script>

</script>

<style>
@font-face {
  font-family: 'Raleway';
  src: url('./assets/fuentes/Raleway-Medium.ttf');
}

/* quita los espacios de la pagina */
body {
    font-family: 'Raleway';
    padding: 0;
    margin: 0;
    
}

.contenedor {
    /* indica que todos los div iran en fila */
    display: inline-block;
    /* cada div le podremos cambiar su ubicación */
    position: absolute;
    /* alto 100% de la página */
    height: 100%;
    /* se pegara al borde superior */
    top: 0px;
}

#contenedor1 {
    background-color: white;
    width: 260px;
    /* se pegara al borde izquierdo */
    left: 0;
    /* tendra un borde de 0 de arriba y abajo y de 20px de derecha a izquierda */
    padding: 0 20px;
}

#contenedor2 {
    background-color: #607D8B;
    /* calcula el tamaño que tendra  500 debido a que el contenedor1 mide 200px y el contenedor3 300px*/
    width: calc(100% - 500px);
    /* separa 300px del lado izquierdo de la pantalla */
    left: 300px;
}

#contenedor3 {
    background-color: #2196F3;
    width: 300px;
    /* 0px del borde derecho */
    right: 0;
}

/* contenedor de color gris */
.card {
    border-radius: 10px;
    background-color: #F5F5F5;
    /* color de texto */
    color: #78909C;
}

/* dentro del contenedor y aplica al menu */
.card .menu {
    /* tamaño de letra */
    font-size: 17px;
    /* se agrega espacios dentro del menu */
    /* 10px espacio de arriba y abajo, 15px de derecha e izquierda */
    padding: 15px 15px;
    /* el puntero del mouse cambia */
    cursor: pointer;
    /* borde izquierdo sin color */
    border-left: 3px solid transparent;
}

/* separacion del icono dentro del menu */
.card .menu i {
    padding: 0 15px 0 0;
}

/* cambio del color de borde */
.card .menu:hover {
    border-left: 3px solid #90A4AE;
}

/* :hover se usa para cambiar al momento de poner el mouse arriba */
.card .menu:hover i {
    /* cambia el color del texto */
    color: #EF6C00;
}

/* aplica al contenedor card con la clase chip */
.card.chip {
    padding: 15px;
    position: relative;
}

/* aplica al icono de adentro */
.card.chip .icon {
    display: inline-block;
    width: 40px;
    height: 40px;
    /* alineación de texto */
    text-align: center;
    /* separación entre lineas */
    line-height: 40px;
    border-radius: 10px;
}

.card.chip .texto {
    /* permite ponerlo en la posicion deseada si el padre tiene position:relative */
    position: absolute;
    top: 10px;
    display: inline-block;
    padding: 5px;
    /* negrita en texto */
    font-weight: 300;
    color: #263238;
}

.card.chip .texto .sub-texto {
    color: #B0BEC5;
    font-size: 14px;
}

#contenedor1-abajo {
    position: absolute;
    bottom: 10px;
    width: 250px;
}

#contenedor1-abajo #doble {
    /* permite colocar los elementos en los bordes del contenedor */
    display: flex;
    justify-content: space-between;
    
}

/* aplica a la clase card dentro de contenedor1-abajo */
#contenedor1-abajo #doble .card {
    display: inline-block;
    width: 80px;
}

#contenedor1-abajo #doble .card .icon {
    display: block;
}

#contenedor1-abajo #doble .card .texto {
    /* se quita la position absolute para regresarlo a su estado normal */
    position: unset;
}

#contenedor1-abajo .card .imagen{
    display: inline-block;
}
#contenedor1-abajo .card .imagen img{
    height: 50px;
    border-radius: 10px;
}


</style>
