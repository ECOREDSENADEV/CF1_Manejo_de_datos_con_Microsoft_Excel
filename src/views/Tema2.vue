<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido(data-aos="flip-up")
      .titulo-principal__numero
        span 2
      h1 Gestión de datos en Excel
    
    .row.mb-5.align-items-center
      .col-lg-4.order-lg-2.mb-3.mb-lg-0
        figure
          img(src="@/assets/curso/tema2/1.png", data-aos="zoom-in")
      .col-lg-8.order-lg-1
        .bg-color-9.p-4(data-aos="fade-left")
          p.mb-0 Una vez comprendida la estructura básica de Excel, el siguiente paso es aprender a trabajar con su elemento central: los datos. La correcta definición de los diferentes tipos de datos, así como la aplicación de formatos adecuados, es fundamental para garantizar la integridad de la información, facilitar su lectura y permitir un análisis eficiente.
    
    separador
    
    .bg-full-width.bg-color-4
      .px-5.mb-5
        #t_2_1.titulo-segundo.color-acento-contenido(data-aos="flip-up")
          h2 2.1 Tipos de datos
        
        p.mb-5 Excel reconoce automáticamente distintos tipos de datos al ingresarlos en una celda, clasificándolos principalmente en: numéricos, texto, fecha/hora, lógicos y errores (Alexander & Walkenbach, 2019). Sin embargo, aunque esta detección es útil, se recomienda verificar y asignar el tipo correcto, ya que esto influye directamente en la forma en que se almacena la información y en las operaciones que pueden realizarse con ella.  A continuación, se presenta un video que explica los tipos de datos más comunes en Excel, detallando sus características, usos y particularidades para una gestión eficiente de la información.

        .row.mb-5.align-items-center
          .col-lg-5.order-lg-2.mb-3.mb-lg-0
            figure
              img(src="@/assets/curso/tema2/2.png", data-aos="zoom-in")
          .col-lg-7.order-lg-1
            .row.justify-content-center.align-items-center.bg-color-10.p-4.tarjeta
              .col-lg-5.mb-3.mb-lg-0
                figure
                  img(src="@/assets/curso/tema2/3.svg", data-aos="zoom-in")
              .col-lg-7
                h2(data-aos="fade-left").mb-4.text-white Pódcast
        
                TarjetaAudio.color-acento-contenido.bg-color-white.mb-3(
                  texto="Tipos de datos "
                  tiempo
                  :audio="require('../assets/curso/podcast/podcast1.mp3')"
                )
    
    p.mb-5 A continuación, se presenta una tabla resumen con los principales tipos de datos que se pueden trabajar en Excel:

    .titulo-sexto.color-acento-contenido
      h5 Tabla 1.
      span Tipos de datos en Excel y ejemplos representativos 
    
    .tabla-a.color-acento-contenido.mb-5 
      table
        thead
          tr
            th.bg-color-2 Tipo de dato
            th.bg-color-2 Descripción
            th.bg-color-2 Ejemplo
        tbody
          tr
            td Texto (general)
            td Cadenas de caracteres alfanuméricos. Se utiliza para etiquetas, nombres, descripciones, etc. Por defecto, Excel alinea el texto a la izquierda.
            td Informe de Ventas, Juan Pérez, ID-005
          tr.bg-color-11
            td Número
            td Valores numéricos con los que se pueden realizar cálculos matemáticos. Incluye enteros, decimales y notación científica. Por defecto, se alinea a la derecha.
            td 1500, 3.1416, 5.25%
          tr
            td Fecha/Hora
            td Valores que representan fechas y horas. Excel los almacena internamente como números de serie, lo que permite realizar cálculos con ellos (ej. calcular días entre dos fechas).
            td 30/09/2025, 11:15 AM, 30/09/2025 11:15
          tr.bg-color-11
            td Booleano
            td Representa un valor lógico de VERDADERO o FALSO. Es el resultado típico de las operaciones de comparación.
            td VERDADERO, FALSO
          tr
            td Fórmula
            td Una expresión que realiza un cálculo y devuelve un resultado. Siempre debe comenzar con el signo igual (=).
            td =A1+B1, =SUMA(C1:C10)
    
    separador
    
    #t_2_2.titulo-segundo.color-acento-contenido(data-aos="flip-up")
      h2 2.2 Principios de formato de celda
    
    p.mb-5 El formato de celda no modifica el valor real de una celda, pero sí transforma su apariencia visual, lo que facilita la lectura, comprensión y análisis de los datos. Es posible acceder a estas opciones haciendo clic derecho sobre una celda o un rango, y seleccionando Formato de celdas.

    .bg-full-width.bg-color-4
      .px-5.mb-5
        .row.justify-content-center
          .col-lg-8
            .bg-color-8.mb-5(data-aos="fade-up")
              .row.justify-content-center.align-items-center
                .col-lg-auto.mb-3.mb-lg-0
                  figure
                    img(src='@/assets/curso/tema2/4.svg', alt='')
                .col-lg
                  .p-4
                    p.mb-0(data-aos="fade-up") Como señala Frye (2013), el formato de una celda define cómo se visualizan los datos sin alterar su valor subyacente, permitiendo al usuario personalizar la presentación mediante distintas categorías como número, alineación, fuente, bordes, relleno y protección.
        
        p.mb-5 A continuación, se presentan  los principales tipos de formato que pueden aplicarse a las celdas en Excel:

        SlyderF.mb-5(columnas="col-lg-6 col-xl-4")
          .tarjeta.bg-color-5.p-4
            .row.justify-content-center.mb-3
              .col-5
                img(src='@/assets/curso/tema2/5.svg' alt='AvatarTop')
            h2.text-center Número
            p.text-center Permite definir cómo se muestran los valores numéricos (número de decimales, separadores de miles, etc.).
          .tarjeta.bg-color-5.p-4
            .row.justify-content-center.mb-3
              .col-5
                img(src='@/assets/curso/tema2/6.svg' alt='AvatarTop')
            h2.text-center Moneda y contabilidad
            p.text-center Aplican el símbolo de moneda y separadores. El formato Contabilidad alinea correctamente los símbolos y decimales en columnas.
          .tarjeta.bg-color-5.p-4
            .row.justify-content-center.mb-3
              .col-5
                img(src='@/assets/curso/tema2/7.svg' alt='AvatarTop')
            h2.text-center Porcentaje
            p.text-center Multiplica el valor de la celda por 100 y lo muestra con el símbolo %.
          .tarjeta.bg-color-5.p-4
            .row.justify-content-center.mb-3
              .col-5
                img(src='@/assets/curso/tema2/8.svg' alt='AvatarTop')
            h2.text-center Fecha y hora
            p.text-center Ofrece múltiples estilos para representar fechas y horas, como dd-mm-aaaa o mmmm d, aaaa.
          .tarjeta.bg-color-5.p-4
            .row.justify-content-center.mb-3
              .col-5
                img(src='@/assets/curso/tema2/9.svg' alt='AvatarTop')
            h2.text-center Personalizado
            p.text-center Permite crear códigos de formato específicos adaptados a necesidades particulares.
          .tarjeta.bg-color-5.p-4
            .row.justify-content-center.mb-3
              .col-5
                img(src='@/assets/curso/tema2/10.svg' alt='AvatarTop')
            h2.text-center Alineación
            p.text-center Controla la posición del contenido dentro de la celda, tanto horizontal como verticalmente. Incluye opciones como Ajustar texto y Combinar y centrar.
          .tarjeta.bg-color-5.p-4
            .row.justify-content-center.mb-3
              .col-5
                img(src='@/assets/curso/tema2/11.svg' alt='AvatarTop')
            h2.text-center Fuente
            p.text-center Permite modificar el tipo, tamaño, color y estilo de la letra (negrita, cursiva, subrayado).
          .tarjeta.bg-color-5.p-4
            .row.justify-content-center.mb-3
              .col-5
                img(src='@/assets/curso/tema2/12.svg' alt='AvatarTop')
            h2.text-center Bordes
            p.text-center Añade líneas alrededor de las celdas o rangos, lo que facilita la organización visual.
          .tarjeta.bg-color-5.p-4
            .row.justify-content-center.mb-3
              .col-5
                img(src='@/assets/curso/tema2/13.svg' alt='AvatarTop')
            h2.text-center Relleno
            p.text-center Cambia el color de fondo de una celda, útil para resaltar encabezados o valores relevante
    
    h3.bg-color-14.d-inline.p-3.tarjeta Actividad práctica
    
    p.mb-5.mt-5 Para consolidar lo aprendido sobre tipos de datos y formatos de celda, se propone la siguiente actividad que permite aplicar estilos visuales y estructurales a una tabla simple en Excel.

    .row.justify-content-center
      .col-lg-10
        div.p-5.bg-color-8
          h4 Tarea paso a paso
          p A continuación, se detallan los pasos que debe seguir en Excel para crear una tabla con distintos tipos de datos y aplicar correctamente los formatos correspondientes.
          ol.lista-ol--cuadro
            li.d-flex
              .lista-ol--cuadro__vineta
                span A
              | Cree la siguiente tabla en una nueva hoja de Excel:
          .titulo-sexto.color-acento-contenido
            h5 Tabla 2.
            span Registro de ventas por producto con distintos tipos de datos
          
          .tabla-a.color-acento-contenido.mb-5
            table
              thead
                tr
                  th.bg-color-2 Producto
                  th.bg-color-2 Fecha de Venta
                  th.bg-color-2 Unidades
                  th.bg-color-2 Precio Unitario
                  th.bg-color-2 Total Venta
              tbody.bg-color-white
                tr
                  td Laptop
                  td 30/09/2025
                  td 5
                  td 2,500,000
                  td 12,500,000
                tr.bg-color-11
                  td Monitor
                  td 29/09/2025
                  td 12
                  td 800,000
                  td 9,600,000
                tr
                  td Teclado
                  td 30/09/2025
                  td 20
                  td 150,000
                  td 3,000,000
          
          ol.lista-ol--cuadro
            li.d-flex
              .lista-ol--cuadro__vineta
                span B
              | Realice los siguientes ajustes de formato:
          
          ul.lista-ul--color.ms-4
            li.mb-0.d-flex
              i.fas.fa-circle-check.bg-color-12
              p.mb-0 Aplique negrita y un color de relleno a la fila de encabezados (primera fila).
            li.mb-0.d-flex
              i.fas.fa-circle-check.bg-color-12
              p.mb-0 Verifique que la columna Fecha de Venta tenga formato de Fecha.
            li.mb-0.d-flex
              i.fas.fa-circle-check.bg-color-12
              p.mb-0 Aplique el formato de Contabilidad (símbolo de peso $, sin decimales) a las columnas Precio Unitario y Total Venta.
            li.mb-0.d-flex
              i.fas.fa-circle-check.bg-color-12
              p.mb-0 Centre horizontal y verticalmente todos los datos de la tabla.
            li.mb-0.d-flex
              i.fas.fa-circle-check.bg-color-12
              p.mb-0 Agregue bordes exteriores e interiores para definir visualmente toda la tabla.
          p.mb-0 Esta actividad permite reforzar la relación entre el tipo de datos ingresado y su visualización adecuada mediante el uso correcto del formato de celda.




</template>

<script>
export default {
  name: 'Tema2',
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
