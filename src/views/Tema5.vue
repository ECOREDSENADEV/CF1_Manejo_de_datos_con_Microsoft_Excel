<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido(data-aos="flip-up")
      .titulo-principal__numero
        span 5
      h1 Formulas y funciones
    
    p Excel permite no solo almacenar datos, sino también realizar cálculos automáticos y estructurados mediante el uso de fórmulas y funciones. Estas herramientas convierten los valores ingresados en resultados útiles, facilitando la gestión, análisis y actualización dinámica de la información.

    separador
    
    .bg-full-width.bg-color-4
      .px-5.mb-5
        #t_5_1.titulo-segundo.color-acento-contenido(data-aos="flip-up")
          h2 5.1 ¿Formula o función?
        
        p.mb-5 Aunque en el uso cotidiano ambos términos pueden confundirse, es importante distinguirlos con claridad, ya que cumplen roles distintos en Excel. A continuación, se explica cada concepto:

        .row.justify-content-center.mb-5
          .col-md-6.col-lg-4.mb-4.mb-lg-0
            .tarjeta--boton.bg-color-8.p-4.h-100
              .row.justify-content-center.mb-3
                .col-5
                  figure
                    img(src='@/assets/curso/tema5/1.svg', alt='Texto que describa la imagen')

              h3.text-center.mb-5 Fórmula
              p.text-center Es una expresión creada manualmente por el usuario, que combina valores, referencias de celda, operadores y, en muchos casos, funciones. Toda fórmula debe comenzar con un signo igual (=).
              h5.text-center Ejemplo: =A1*1.19

          .col-md-6.col-lg-4.mb-4.mb-lg-0
            .tarjeta--boton.bg-color-13.p-4.h-100
              .row.justify-content-center.mb-3
                .col-5
                  figure
                    img(src='@/assets/curso/tema5/2.svg', alt='Texto que describa la imagen')

              h3.text-center.mb-5 Función
              p.text-center Es una fórmula predeterminada y nombrada por Excel, diseñada para realizar tareas específicas. Las funciones facilitan la ejecución de cálculos complejos, extensos o especializados.
              h5.text-center Ejemplo: =SUMA(A1:A10) en lugar de escribir =A1+A2+A3+...+A10

        p Según Frye (2019), la diferencia esencial radica en que las fórmulas son diseñadas por el usuario para responder a necesidades particulares, mientras que las funciones son herramientas prediseñadas por Excel para realizar operaciones comunes de forma más rápida y eficiente. Además, una fórmula puede incluir una o varias funciones.

    separador
    
    #t_5_2.titulo-segundo.color-acento-contenido(data-aos="flip-up")
      h2 5.2 Sintaxis y proceso de creación
    
    p.mb-5 Para que una función se ejecute correctamente en Excel, debe seguir una estructura específica llamada sintaxis. Esta estructura comienza siempre con un signo igual, seguido del nombre de la función y un conjunto de argumentos encerrados entre paréntesis. La sintaxis general es la siguiente:

    .row.justify-content-center.mb-5
      .col-lg-5
        .bg-color-5.p-4.text-center
          h5.mb-0 =NOMBRE_FUNCION(argumento1; argumento2; ...)

    .bg-full-width.bg-color-4
      .px-5.mb-5
        p.mb-5 Los argumentos pueden ser valores constantes, referencias de celda, rangos, otras funciones (funciones anidadas) o expresiones (Winston, 2019). Algunas funciones no requieren argumentos, y otras aceptan argumentos opcionales.

        .row.justify-content-center
          .col-lg-8
            .titulo-sexto.color-acento-contenido
              h5 Tabla 9.
              span Elementos de la sintaxis de una función en Excel
            
            .tabla-a.color-acento-contenido.mb-5 
              table
                thead
                  tr
                    th.bg-color-2 Elemento
                    th.bg-color-2 Descripción
                tbody.bg-color-white
                  tr
                    td Signo igual (=)
                    td Indica a Excel que se va a introducir una fórmula o función.
                  tr.bg-color-11
                    td Nombre de la función
                    td Es el nombre específico de la función, como SUMA, PROMEDIO, SI, etc.
                  tr
                    td Paréntesis ()
                    td Encierran los argumentos que necesita la función para funcionar.
                  tr.bg-color-11
                    td Argumentos
                    td Son los valores, referencias o rangos necesarios para que la función realice su cálculo. Se separan con punto y coma (;) o coma (,), según la configuración regional.

        .titulo-con-imagen.mb-5(data-aos="fade-right")
          .titulo-con-imagen__fondo
            img.titulo-con-imagen__imagen(src="@/assets/componentes/1.svg")
            h3.titulo-con-imagen__texto Proceso para crear una función en Excel
        
        p.mb-5 A continuación, se describen los pasos básicos que deben seguirse para insertar correctamente una función en Excel, ya sea escribiéndola manualmente o utilizando el asistente integrado:

        .row.justify-content-center
          .col-lg-10
            .bg-color-8.mb-5(data-aos="fade-down")
              .row.justify-content-center.align-items-center
                .col-lg-auto.mb-3.mb-lg-0
                  figure
                    img(src='@/assets/curso/tema5/3.png', alt='')
                .col-lg
                  .p-4
                    ol.lista-ol--cuadro
                      li.d-flex
                        .lista-ol--cuadro__vineta
                          span A
                        | Seleccionar la celda: haga clic en la celda donde desea mostrar el resultado.
                      li.d-flex
                        .lista-ol--cuadro__vineta
                          span B
                        | Iniciar la fórmula: escriba el signo igual (=).
                      li.d-flex
                        .lista-ol--cuadro__vineta
                          span C
                        | Insertar la función, de dos formas posibles:
                    ul.lista-ul--color.mb-0.ms-4
                      li.mb-2.d-flex
                        i.fas.fa-circle-check.bg-color-12
                        p.mb-0 Escribiendo directamente: comience a escribir el nombre de la función. Excel desplegará una lista de sugerencias (IntelliSense). Haga doble clic en la opción deseada.
                      li.mb-2.d-flex
                        i.fas.fa-circle-check.bg-color-12
                        p.mb-0 Usando el asistente: vaya a la pestaña Fórmulas y haga clic en Insertar función (fx). Se abrirá un cuadro de diálogo donde podrá buscar funciones por categoría e ingresar los argumentos paso a paso.
                    ol.lista-ol--cuadro
                      li.d-flex
                        .lista-ol--cuadro__vineta
                          span D
                        | Introducir los argumentos: seleccione las celdas o escriba los valores necesarios.
                      li.d-flex
                        .lista-ol--cuadro__vineta
                          span E
                        | Cerrar paréntesis y presionar Enter: complete la función cerrando el paréntesis y pulse Enter para obtener el resultado.
    
    separador
    
    #t_5_3.titulo-segundo.color-acento-contenido(data-aos="flip-up")
      h2 5.3 Catálogo de funciones predeterminadas esenciales
    
    p.mb-5 Excel cuenta con una variedad de funciones. A continuación se presentan algunas de las más utilizadas y fundamentales.

    .bg-full-width.bg-color-4
      .px-5.mb-5
        .row.justify-content-center.mb-5
          .col-lg-10
            AcordionA(tipo="a" clase-tarjeta="tarjeta bg-color-5")
              div(titulo="Funciones matemáticas y estadísticas").justify-content-center
                ul.lista-ul--color.mb-0.ms-5
                  li.mb-2.d-flex
                    i.fas.fa-circle-check.bg-color-12
                    p.mb-0 SUMA(rango): Suma todos los números en un rango de celdas.
                  li.mb-2.d-flex
                    i.fas.fa-circle-check.bg-color-12
                    p.mb-0 PROMEDIO(rango): Calcula el promedio (media aritmética) de los números en un rango.
                  li.mb-2.d-flex
                    i.fas.fa-circle-check.bg-color-12
                    p.mb-0 CONTAR(rango): Cuenta cuántas celdas contienen números en un rango.
                  li.mb-2.d-flex
                    i.fas.fa-circle-check.bg-color-12
                    p.mb-0 MAX(rango): Devuelve el valor más alto en un rango.
                  li.mb-2.d-flex
                    i.fas.fa-circle-check.bg-color-12
                    p.mb-0 MIN(rango): Devuelve el valor más bajo en un rango.
              div(titulo="Función lógica").justify-content-center
                p.ms-5 SI(prueba_logica; valor_si_verdadero; valor_si_falso): Es una de las funciones más potentes. Evalúa una condición (prueba_logica). Si la condición es VERDADERA, devuelve un valor; si es FALSA, devuelve otro.
                p.ms-5 Ejemplo: =SI(A1>=18; "Mayor de edad"; "Menor de edad").
              div(titulo="Funciones de texto").justify-content-center
                ul.lista-ul--color.mb-0.ms-5
                  li.mb-2.d-flex
                    i.fas.fa-circle-check.bg-color-12
                    p.mb-0 CONCAT(texto1; texto2; ...): Une varias cadenas de texto en una sola (alternativa al operador &).
                  li.mb-2.d-flex
                    i.fas.fa-circle-check.bg-color-12
                    p.mb-0 IZQUIERDA(texto; num_caracteres): Devuelve el número especificado de caracteres desde el inicio de una cadena de texto.
                  li.mb-2.d-flex
                    i.fas.fa-circle-check.bg-color-12
                    p.mb-0 DERECHA(texto; num_caracteres): Devuelve el número especificado de caracteres desde el final de una cadena de texto.
                  li.mb-2.d-flex
                    i.fas.fa-circle-check.bg-color-12
                    p.mb-0 LARGO(texto): Devuelve el número de caracteres en una cadena de texto.
              div(titulo="Funciones de fecha y hora").justify-content-center
                ul.lista-ul--color.mb-0.ms-5
                  li.mb-2.d-flex
                    i.fas.fa-circle-check.bg-color-12
                    p.mb-0 HOY(): Devuelve la fecha actual. No requiere argumentos.
                  li.mb-2.d-flex
                    i.fas.fa-circle-check.bg-color-12
                    p.mb-0 AHORA(): Devuelve la fecha y hora actuales. No requiere argumentos.

        h3.bg-color-14.d-inline.p-3.tarjeta Actividad práctica
        p.mb-5.mt-5 Para afianzar el uso de funciones básicas en Excel, se propone una actividad que permite aplicar operaciones comunes sobre un conjunto de datos sencillo.

    .row.justify-content-center
      .col-lg-7
        .titulo-sexto.color-acento-contenido
          h5 Tabla 10.
          span Ventas por vendedor en el mes de enero
        
        .tabla-a.color-acento-contenido.mb-5.pst
          table
            thead
              tr
                th.bg-color-2 Vendedor
                th.bg-color-2 Ventas Enero
            tbody
              tr
                td Ana
                td 5,200,000
              tr
                td Luis
                td 4,800,000
              tr
                td Carlos
                td 6,100,000
              tr
                td María
                td 3,900,000
              tr
                td Sofía
                td 5,500,000
      .col-lg-3
        figure.mb-5
          img(src="@/assets/curso/tema5/4.svg", data-aos="zoom-in")

    .row.justify-content-center
      .col-lg-10
        .bg-color-8.mb-5(data-aos="fade-down")
          .row.justify-content-center.align-items-center
            .col-lg-auto.mb-3.mb-lg-0
              figure
                img(src='@/assets/curso/tema5/5.png', alt='')
            .col-lg
              .p-4
                h4 Tarea paso a paso
                p A continuación, se detallan las acciones que deberá realizar en Excel para aplicar correctamente las funciones indicadas sobre el conjunto de datos proporcionado.
                ol.lista-ol--cuadro
                  li.d-flex
                    .lista-ol--cuadro__vineta
                      span A
                    | Recree la tabla anterior.
                  li.d-flex
                    .lista-ol--cuadro__vineta
                      span B
                    | Debajo de la tabla, calcule lo siguiente utilizando funciones de Excel:
                ul.lista-ul--color.mb-0.ms-5
                  li.mb-2.d-flex
                    i.fas.fa-circle-check.bg-color-12
                    p.mb-0 Total de Ventas: (Use SUMA).
                  li.mb-2.d-flex
                    i.fas.fa-circle-check.bg-color-12
                    p.mb-0 Venta Promedio: (Use PROMEDIO).
                  li.mb-2.d-flex
                    i.fas.fa-circle-check.bg-color-12
                    p.mb-0 Venta Más Alta: (Use MAX).
                  li.mb-2.d-flex
                    i.fas.fa-circle-check.bg-color-12
                    p.mb-0 Venta Más Baja: (Use MIN).
                  li.mb-2.d-flex
                    i.fas.fa-circle-check.bg-color-12
                    p.mb-0 Número de Vendedores: (Use CONTAR).
                ol.lista-ol--cuadro
                  li.d-flex
                    .lista-ol--cuadro__vineta
                      span C
                    | En una nueva columna llamada "Comisión", utilice la función SI para calcular una comisión del 10% para cada vendedor cuyas ventas superen los 5,000,000. Si no superan ese valor, la comisión debe ser 0. La fórmula sería algo como: =SI(B2>5000000; B2*0.1; 0).



</template>

<script>
export default {
  name: 'Tema5',
  data: () => ({
    // variables de vue
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
