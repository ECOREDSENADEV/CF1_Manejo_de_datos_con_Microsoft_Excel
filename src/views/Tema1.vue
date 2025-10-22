<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido(data-aos="flip-up")
      .titulo-principal__numero
        span 1
      h1 Interfaz y estructura de Excel
    
    .bg-full-width.bg-color-4
      .px-5.mb-5
        p Para trabajar eficazmente con Microsoft Excel, es necesario comprender tanto la estructura de los archivos como los elementos que conforman su interfaz. A continuación, se aborda los conceptos clave que permiten organizar, manipular y analizar datos dentro del entorno de Excel.

        separador
        
        #t_1_1.titulo-segundo.color-acento-contenido(data-aos="flip-up")
          h2 1.1 Conceptos fundamentales 

        .row.mb-5
          .col-lg-4.order-lg-2.mb-3.mb-lg-0
            figure
              img(src="@/assets/curso/tema1/1.png", data-aos="zoom-in")
          .col-lg-8.order-lg-1
            .bg-color-2.p-3.mb-3
              p.mb-0(data-aos="fade-left") Microsoft Excel es una aplicación de hoja de cálculo que organiza la información en una estructura bidimensional compuesta por filas y columnas. La intersección entre ambas genera una celda, que constituye la unidad básica de almacenamiento de datos (Walkenbach, 2013).
            p Un libro de trabajo está compuesto por una o más hojas de cálculo, cada una con capacidad para hasta 1,048,576 filas y 16,384 columnas (Microsoft Corporation, 2021). Las filas se identifican numéricamente (1, 2, 3...) y las columnas alfabéticamente (A, B, C... AA, AB...), lo que permite referenciar cada celda de manera única (por ejemplo, A1, B5, C10).
            .row.justify-content-center
              .col-md-10
                div.bg-color-3.p-3(data-aos="fade-up").text-center
                  p.mb-0 La estructura jerárquica de Excel puede representarse como:
                  h5.mb-0 Aplicación → Libro de trabajo → Hoja de cálculo → Celda

        p.mb-5 Esta organización facilita el manejo de grandes volúmenes de información de forma estructurada y permite realizar cálculos y análisis complejos.

        .titulo-con-imagen.mb-5(data-aos="fade-right")
          .titulo-con-imagen__fondo
            img.titulo-con-imagen__imagen(src="@/assets/componentes/1.svg")
            h3.titulo-con-imagen__texto Elementos clave en la estructura de Excel

    p.mb-5 Para comprender plenamente cómo se organiza y opera Excel, es necesario identificar los componentes básicos que conforman su arquitectura. A continuación se presentan los elementos principales, sus nombres y funciones dentro del entorno de trabajo:

    .row.justify-content-center
      .col-lg-10
        .titulo-sexto.color-acento-contenido
          h5 Figura 1.
          span Elementos clave en la estructura de Excel

    .bg-full-width.bg-color-4
      .px-5.mb-5
        .row.justify-content-center
          .col-lg-10
            figure
              img(src="@/assets/curso/tema1/2.png", data-aos="zoom-in", alt="Captura de pantalla de una hoja de cálculo en Excel con etiquetas que identifican elementos básicos como libro de trabajo, hoja de cálculo, fila, columna, celda, celda activa y rango seleccionado. ")
        

    .row.align-items-center.mb-5
      .col-lg-4.mb-3.mb-lg-0
        figure
          img(src="@/assets/curso/tema1/3.png", alt="").mb-4.mb-lg-0
      .col-lg-8
        AcordionA(tipo="a" clase-tarjeta="tarjeta bg-color-5")
          .div(titulo="Libro de trabajo")
            p Archivo principal con extensión .xlsx. Actúa como un contenedor de hojas de cálculo relacionadas (Microsoft Corporation, 2025).
    
          .div(titulo="Hoja de cálculo")
            p También llamada worksheet. Es la cuadrícula principal donde se introducen y manipulan datos. Se pueden agregar, eliminar o reorganizar hojas dentro del libro.
    
          .div(titulo="Columna")
            p Conjunto vertical de celdas. Se identifican con letras (A, B, C...).
    
          .div(titulo="Fila")
            p Conjunto horizontal de celdas. Se identifican con números (1, 2, 3...).
          .div(titulo="Celda")
            p Intersección de una fila y una columna. Unidad mínima de almacenamiento de datos. Se identifica mediante su referencia de celda (ej. B4).
          .div(titulo="Celda activa")
            p Celda seleccionada actualmente. Se distingue por un borde más grueso.
          .div(titulo="Rango")
            p Conjunto rectangular de celdas. Se define por dos referencias separadas por dos puntos, como A2:E13 (desde la esquina superior izquierda a la inferior derecha).
    
    separador
    
    #t_1_2.titulo-segundo.color-acento-contenido(data-aos="flip-up")
      h2 1.2 Interfaz de usuario
    
    p.mb-5 La interfaz de Excel está diseñada para facilitar el acceso a sus múltiples herramientas y funcionalidades mediante una organización visual intuitiva. Los componentes principales de la interfaz son: 

    .titulo-sexto.color-acento-contenido
      h5 Figura 2.
      span Elementos principales de la interfaz de Excel
    
    .bg-full-width.bg-color-4
      .px-5.mb-5
        figure.mb-5
          img(src="@/assets/curso/tema1/4.png", data-aos="zoom-in", alt="Captura de pantalla de la interfaz de Excel con etiquetas que señalan la barra de acceso rápido, la cinta de opciones con pestañas y herramientas agrupadas, y la barra de fórmulas ubicada debajo para editar el contenido de las celdas. ")
    
        .row.justify-content-center
          .col-sm-6.col-lg-4.mb-4.mb-lg-0
            .tarjeta--boton.bg-color-6.p-4.h-100
              h4.bg-color-7.mb-3 A
              h3.text-center Barra de acceso rápido
              p.text-center Situada en la esquina superior izquierda. Incluye por defecto los comandos Guardar, Deshacer y Rehacer, pero puede personalizarse agregando los comandos que el usuario utiliza con mayor frecuencia, sin depender de la pestaña activa.

          .col-sm-6.col-lg-4.mb-4.mb-lg-0
            .tarjeta--boton.bg-color-6.p-4.h-100
              h4.bg-color-7.mb-3 B
              h3.text-center Cinta de opciones 
              p.text-center Es la barra de herramientas principal ubicada en la parte superior de la ventana. Organiza los comandos en pestañas lógicas (Inicio, Insertar, Fórmulas, Datos), que a su vez se subdividen en grupos de comandos relacionados (por ejemplo, Fuente, Alineación, Número en la pestaña Inicio). Esta estructura permite localizar rápidamente las herramientas necesarias (Frye, 2019).

          .col-sm-6.col-lg-4.mb-4.mb-sm-0
            .tarjeta--boton.bg-color-6.p-4.h-100
              h4.bg-color-7.mb-3 C
              h3.text-center Barra de fórmulas
              p.text-center Se encuentra justo debajo de la cinta de opciones. Tiene dos funciones: (1) Mostrar el contenido real de la celda activa (ya sea texto, número o fórmula), y (2) Permitir la introducción o edición de datos y fórmulas directamente en la celda activa.

    h3.bg-color-14.d-inline.p-3.tarjeta Actividad práctica
    
    p.mb-5.mt-5 Para reforzar la comprensión de los elementos clave de la interfaz de Excel, se propone la siguiente actividad, que permite al usuario explorar directamente las funciones descritas:

    .row.justify-content-center
      .col-lg-10
        .bg-color-8.mb-5(data-aos="fade-down")
          .row.justify-content-center.align-items-center
            .col-lg-auto.mb-3.mb-lg-0
              figure
                img(src='@/assets/curso/tema1/5.png', alt='')
            .col-lg
              .p-4
                h4 Tarea paso a paso
                p Realice las siguientes acciones en Excel para familiarizarse con la interfaz y aplicar los conceptos básicos aprendidos.
                ol.lista-ol--cuadro
                  li.d-flex
                    .lista-ol--cuadro__vineta
                      span A
                    | Abra un nuevo libro de trabajo en Excel.
                  li.d-flex
                    .lista-ol--cuadro__vineta
                      span B
                    | Cambie el nombre de la hoja "Hoja1" a MiPrimeraHoja.
                  li.d-flex
                    .lista-ol--cuadro__vineta
                      span C
                    | Agregue dos hojas nuevas y nómbrelas Datos y Reporte.
                  li.d-flex
                    .lista-ol--cuadro__vineta
                      span D
                    | En la hoja MiPrimeraHoja, seleccione la celda C3 y escriba su nombre. Observe cómo el contenido aparece tanto en la celda como en la barra de fórmulas.
                  li.d-flex
                    .lista-ol--cuadro__vineta
                      span E
                    | Seleccione el rango de celdas desde A1 hasta D10.
                  li.d-flex
                    .lista-ol--cuadro__vineta
                      span F
                    | Personalice la Barra de acceso rápido agregando el comando Ordenar ascendente.
                  

           



</template>

<script>
export default {
  name: 'Tema1',
  data: () => ({
    mostrarIndicadorTarjetaAudio: true,
  }),
  mounted() {
    this.$nextTick(() => {
      this.$aosRefresh()
    })
  },
  updated() {
    this.$aosRefresh()
  },
}
</script>

<style lang="sass"></style>
