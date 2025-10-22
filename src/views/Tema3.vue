<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido(data-aos="flip-up")
      .titulo-principal__numero
        span 3
      h1 Referencias de celda
    
    p.mb-5 Las referencias de celda son el pilar fundamental sobre el que se construyen las fórmulas en Excel. Comprender cómo funcionan y cómo se comportan al copiar o mover fórmulas es una de las habilidades clave para avanzar de un nivel básico a un uso eficiente y profesional de la herramienta.

    .bloque-texto-g.color-secundario.p-3.p-sm-4.p-md-5.mb-5
      .bloque-texto-g__img(
        :style="{'background-image': `url(${require('@/assets/curso/tema3/1.png')})`}"
      )(data-aos="zoom-in")
      .bloque-texto-g__texto.p-4
        p.mb-0 Una referencia de celda identifica de manera única una celda o un rango de celdas dentro de una hoja de cálculo. Gracias a ello, se puede utilizar su contenido dentro de fórmulas y funciones (Walkenbach, 2013). Además, son indispensables para la creación de fórmulas dinámicas, ya que permiten que los cálculos se actualicen automáticamente cuando cambian los valores referenciados.
    

    .row.align-items-center
      .col-lg-auto.order-2
        img(src="@/assets/curso/tema3/2.svg", style="max-width: 90px").mx-auto
      .col-lg.order-1.mb-3.mb-lg-0
        p.mb-0 El uso de referencias, en lugar de ingresar valores constantes, proporciona mayor flexibilidad y facilita el mantenimiento de hojas de cálculo complejas. Como explican Alexander & Walkenbach (2019), una de las principales ventajas es que al modificar el valor de una celda referenciada, todas las fórmulas que dependen de ella se recalculan de manera automática.
    
    .bg-full-width.bg-color-4
      .px-5.mb-5
        separador
        
        #t_3_1.titulo-segundo.color-acento-contenido(data-aos="flip-up")
          h2 3.1 Concepto y utilidad de las referencias
        
        p.mb-5 Una referencia de celda (por ejemplo, A1) permite identificar una celda específica dentro de la hoja de cálculo para que su contenido pueda ser usado en una fórmula. Esto hace posible construir fórmulas basadas en los valores de otras celdas.

        .row.justify-content-center
          .col-lg-10
            .bg-color-8.mb-5(data-aos="fade-down")
              .row.justify-content-center.align-items-center
                .col-lg-auto.mb-3.mb-lg-0
                  figure
                    img(src='@/assets/curso/tema3/3.png', alt='')
                .col-lg
                  .p-4
                    p.mb-0 Por ejemplo, en lugar de escribir una fórmula con valores fijos como =10+20, se puede escribir =A1+A2, donde la celda A1 contiene el número 10 y A2 contiene 20. La principal ventaja es que, si los valores en A1 o A2 cambian, el resultado de la fórmula se actualiza automáticamente, sin necesidad de editarla.
        
        p Este principio de actualización automática es lo que convierte a Excel en una herramienta tan potente para el análisis de datos y la construcción de modelos dinámicos.
    
    separador
    
    #t_3_2.titulo-segundo.color-acento-contenido(data-aos="flip-up")
      h2 3.2 Tipos de referencias
    
    p Excel ofrece tres tipos de referencias de celda, y su diferencia se hace evidente cuando una fórmula es copiada o arrastrada a otra ubicación (Alexander et al., 2018). Comprender cómo se comportan estas referencias es esencial para controlar correctamente los cálculos y evitar errores en hojas de cálculo complejas.
    p.mb-5 A continuación, se presentan los tres tipos de referencias, su sintaxis, comportamiento y uso más adecuado:

    .titulo-sexto.color-acento-contenido
      h5 Tabla 3.
      span Comparación de los tipos de referencias en Excel 
    
    .tabla-a.color-acento-contenido.mb-5 
      table
        thead
          tr
            th.bg-color-2 Tipo de referencia
            th.bg-color-2 Sintaxis
            th.bg-color-2 Comportamiento al copiar fórmulas
            th.bg-color-2 Uso ideal
        tbody
          tr
            td Relativa
            td A1
            td Se ajusta automáticamente a la nueva posición. Ejemplo: =A1+B1 en C1 se convierte en =A2+B2 al copiar a C2.
            td Cuando se desea repetir un cálculo en varias filas o columnas.
          tr
            td Absoluta
            td $A$1
            td Se mantiene fija al copiar la fórmula; no se adapta a la nueva posición.
            td Cuando se necesita hacer referencia a un valor constante, como una tasa fija o celda clave.
          tr
            td Mixta
            td $A1 o A$1
            td Solo una parte (columna o fila) se mantiene fija. =A$1 fija la fila 1; =$A1 fija la columna A.
            td Ideal para tablas de doble entrada o fórmulas que combinan elementos fijos y variables.

    .titulo-con-imagen.mb-5(data-aos="fade-right")
      .titulo-con-imagen__fondo
        img.titulo-con-imagen__imagen(src="@/assets/componentes/1.svg")
        h3.titulo-con-imagen__texto Caso de uso: cálculo del IVA con referencia absoluta
    
    p.mb-5 Supongamos que tienes una lista de precios en la columna A y una tasa de IVA del 19% ubicada en la celda E1. Si deseas calcular el valor del IVA para cada producto en la columna B, puedes usar la siguiente fórmula: 
      span.etiqueta  <b>=A2*$E$1</b>
    
    .titulo-sexto.color-acento-contenido
      h5 Figura 3.
      span Cálculo del IVA mediante una referencia absoluta en Excel.
    
    .row.mb-5
      .col-lg-6
        figure.mb-5
          img(src="@/assets/curso/tema3/4.png", data-aos="zoom-in", alt='Captura de pantalla de una hoja de cálculo en Excel con una fórmula en la celda B2 que multiplica el valor de A2 por la celda E1, utilizando referencia absoluta. Incluye columnas con encabezados "Precio", "IVA" y "Tasa IVA", y valores numéricos ingresados.')
      .col-lg-6
        .bg-color-9.p-5
          ul.lista-ul--color.ms-3
            li.mb-0.d-flex
              i.fas.fa-circle-check.bg-color-12
              p.mb-0 A2 es una referencia relativa que cambiará a A3, A4, etc., al copiar la fórmula hacia abajo.
            li.mb-0.d-flex
              i.fas.fa-circle-check.bg-color-12
              p.mb-0 $E$1 es una referencia absoluta, que siempre apuntará a la celda donde está la tasa del IVA, sin importar dónde se copie la fórmula.
    
    p.mb-5 Este ejemplo ilustra cómo las referencias combinadas permiten automatizar cálculos y mantener la lógica correcta sin necesidad de reescribir fórmulas.

    separador
    
    .bg-full-width.bg-color-4
      .px-5.mb-5
        #t_3_3.titulo-segundo.color-acento-contenido(data-aos="flip-up")
          h2 3.3 Procedimiento de creación y modificación
        
        p.mb-5 En Excel, las referencias pueden crearse y modificarse fácilmente mientras se construyen fórmulas. Esta capacidad permite construir cálculos dinámicos y eficientes, esenciales para automatizar tareas.

        .titulo-con-imagen.mb-5(data-aos="fade-right")
          .titulo-con-imagen__fondo
            img.titulo-con-imagen__imagen(src="@/assets/componentes/1.svg")
            h3.titulo-con-imagen__texto Creación de referencias
        
        p.mb-5 Existen dos maneras principales de crear una referencia en una fórmula:

        .row.justify-content-center
          .col-md-6.col-lg-4.mb-4.mb-lg-0
            .tarjeta--boton.bg-color-8.p-4.h-100
              .row.justify-content-center.mb-3
                .col-7
                  figure
                    img(src='@/assets/curso/tema3/5.svg', alt='Texto que describa la imagen')

              h3.text-center.mb-5 Manual
              p.text-center Escribiendo directamente la dirección de la celda (por ejemplo, A1) en la barra de fórmulas.

          .col-md-6.col-lg-4.mb-4.mb-lg-0
            .tarjeta--boton.bg-color-13.p-4.h-100
              .row.justify-content-center.mb-3
                .col-7
                  figure
                    img(src='@/assets/curso/tema3/6.svg', alt='Texto que describa la imagen')

              h3.text-center.mb-5 Interactiva
              p.text-center Haciendo clic sobre la celda deseada mientras se está editando una fórmula. Excel resalta la celda seleccionada con un color específico, lo que facilita su identificación visual (Dodge et al., 2018).
    
    .titulo-con-imagen.mb-5(data-aos="fade-right")
      .titulo-con-imagen__fondo
        img.titulo-con-imagen__imagen(src="@/assets/componentes/1.svg")
        h3.titulo-con-imagen__texto Modificación entre tipos de referencia

    p.mb-5 Una vez escrita una fórmula, se puede cambiar el tipo de referencia (relativa, absoluta o mixta) de manera rápida utilizando la tecla <b>F4</b>:

    .row.mb-5
      .col-lg-6.order-lg-2.mb-3.mb-lg-0
        figure
          img(src="@/assets/curso/tema3/7.png", data-aos="zoom-in")
      .col-lg-6.order-lg-1
        .bg-color-3.p-4(data-aos="fade-left").text-center
          p Al posicionar el cursor sobre una referencia en la fórmula y presionar F4, Excel cicla entre los siguientes estados:
          h5.bg-color-5.p-3 A1 → $A$1 → A$1 → $A1 → A1
          p Este atajo permite modificar rápidamente el comportamiento de la referencia sin necesidad de escribir manualmente los símbolos $.
    
   
    h3.bg-color-14.d-inline.p-3.tarjeta Actividad práctica
    
    p.mb-5.mt-5 Para afianzar el uso correcto de referencias relativas y absolutas, se propone la siguiente actividad, que permite aplicar estos conceptos en un ejemplo práctico de cálculo automatizado:

    .bg-full-width.bg-color-4
      .px-5.mb-5
        .row.justify-content-center
          .col-lg-10
            .bg-color-8.mb-5(data-aos="fade-down")
              .row.justify-content-center.align-items-center
                .col-lg-auto.mb-3.mb-lg-0
                  figure
                    img(src='@/assets/curso/tema3/8.png', alt='')
                .col-lg
                  .p-4
                    h4 Tarea paso a paso
                    p Siga las instrucciones que se indican a continuación para aplicar correctamente referencias relativas y absolutas en una fórmula y automatizar el cálculo de resultados en Excel.
                    ol.lista-ol--cuadro
                      li.d-flex
                        .lista-ol--cuadro__vineta
                          span A
                        | Configure una hoja con la siguiente información:
                    ul.lista-ul--color.ms-4
                      li.mb-0.d-flex
                        i.fas.fa-circle-check.bg-color-12
                        p.mb-0 En la celda A1, escriba "Valor".
                      li.mb-0.d-flex
                        i.fas.fa-circle-check.bg-color-12
                        p.mb-0 En las celdas A2 a A6, escriba los números 10, 20, 30, 40, 50.
                      li.mb-0.d-flex
                        i.fas.fa-circle-check.bg-color-12
                        p.mb-0 En la celda C1, escriba "Multiplicador".
                      li.mb-0.d-flex
                        i.fas.fa-circle-check.bg-color-12
                        p.mb-0 En la celda D1, escriba el número 5.
                      li.mb-0.d-flex
                        i.fas.fa-circle-check.bg-color-12
                        p.mb-0 En la celda B1, escriba "Resultado".
                    ol.lista-ol--cuadro
                      li.d-flex
                        .lista-ol--cuadro__vineta
                          span B
                        | En la celda B2, escriba una única fórmula que multiplique el valor de la celda A2 por el multiplicador que se encuentra en D1. Asegúrese de usar los tipos de referencia correctos.
                      li.d-flex
                        .lista-ol--cuadro__vineta
                          span C
                        | Copie y arrastre la fórmula de B2 hacia abajo hasta la celda B6. Si usó las referencias correctas, todos los cálculos deberían ser correctos (50, 100, 150, 200, 250).
    
    



</template>

<script>
export default {
  name: 'Tema3',
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
