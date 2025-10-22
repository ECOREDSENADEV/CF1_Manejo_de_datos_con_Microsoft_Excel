<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido(data-aos="flip-up")
      .titulo-principal__numero
        span 4
      h1 Operadores para la creación de formulas
    
    p Los operadores son símbolos que indican el tipo de cálculo que Excel debe realizar dentro de una fórmula. Son, en esencia, los verbos de las fórmulas: conectan valores, referencias y expresiones para producir resultados nuevos y dinámicos.

    separador
    
    #t_4_1.titulo-segundo.color-acento-contenido(data-aos="flip-up")
      h2 4.1 Concepto y tipos de operadores
    
    p.mb-5 Excel dispone de varios tipos de operadores, cada uno con una función específica en el procesamiento de datos (Winston, 2021). Estos se clasifican en cuatro categorías principales: aritméticos, de comparación, de concatenación de texto y de referencia.

    .row.justify-content-center
      .col-lg-10
        AcordionA(tipo="a" clase-tarjeta="tarjeta bg-color-5")
          .row(titulo="Operadores aritméticos").justify-content-center
            .col-lg-11
              p Estos operadores se utilizan para realizar cálculos matemáticos básicos.
              .titulo-sexto.color-acento-contenido
                h5 Tabla 4.
                span Operadores aritméticos en Excel 
              
              .tabla-a.color-acento-contenido.mb-5 
                table
                  thead
                    tr
                      th.bg-color-2 Operador
                      th.bg-color-2 Nombre
                      th.bg-color-2 Ejemplo
                      th.bg-color-2 Resultado
                  tbody.bg-color-white
                    tr
                      td +
                      td Suma
                      td = 5 + 3
                      td 8
                    tr.bg-color-11
                      td -
                      td Resta
                      td = 5 - 3
                      td 2
                    tr
                      td *
                      td Multiplicación
                      td = 5 * 3
                      td 15
                    tr.bg-color-11
                      td /
                      td División
                      td = 15 / 3
                      td 5
                    tr
                      td %
                      td Porcentaje
                      td = 20%
                      td 0.2
                    tr.bg-color-11
                      td ^
                      td Exponenciación
                      td = 5 ^ 2
                      td 25
          .row(titulo="Operadores de comparación").justify-content-center
            .col-lg-11
              p Se usan para comparar dos valores. Siempre devuelven un resultado lógico: VERDADERO o FALSO.
              .titulo-sexto.color-acento-contenido
                h5 Tabla 5.
                span Operadores de comparación
              
              .tabla-a.color-acento-contenido.mb-5 
                table
                  thead
                    tr
                      th.bg-color-2 Operador
                      th.bg-color-2 Nombre
                      th.bg-color-2 Ejemplo
                      th.bg-color-2 Resultado
                  tbody.bg-color-white
                    tr
                      td =
                      td Igual a
                      td = 5 = 3
                      td FALSO
                    tr.bg-color-11
                      td >
                      td Mayor que
                      td = 5 > 3
                      td VERDADERO
                    tr
                      td <
                      td Menor que
                      td = 5 < 3
                      td FALSO
                    tr.bg-color-11
                      td >=
                      td Mayor o igual que
                      td = 5 >= 5
                      td VERDADERO
                    tr
                      td <=
                      td Menor o igual que
                      td = 5 <= 3
                      td FALSO
                    tr.bg-color-11
                      td <>
                      td Diferente de
                      td = 5 <> 3
                      td VERDADERO

          .row(titulo="Operadores de concatenación de texto").justify-content-center
            .col-lg-11
              p Este operador se utiliza para unir (concatenar) cadenas de texto.
              .titulo-sexto.color-acento-contenido
                h5 Tabla 6.
                span Operador de concatenación de texto 
              
              .tabla-a.color-acento-contenido.mb-5 
                table
                  thead
                    tr
                      th.bg-color-2 Operador
                      th.bg-color-2 Nombre
                      th.bg-color-2 Ejemplo
                      th.bg-color-2 Resultado
                  tbody.bg-color-white
                    tr
                      td &
                      td Ampersand
                      td ="Juan"&" "&"Pérez"
                      td "Juan Pérez"
                    
          .row(titulo="Operadores de referencia").justify-content-center
            .col-lg-11
              p Estos operadores combinan rangos de celdas para utilizarlos en funciones o fórmulas.
              .titulo-sexto.color-acento-contenido
                h5 Tabla 7.
                span Operadores de referencia
              
              .tabla-a.color-acento-contenido.mb-5 
                table
                  thead
                    tr
                      th.bg-color-2 Operador
                      th.bg-color-2 Nombre
                      th.bg-color-2 Descripción
                      th.bg-color-2 Ejemplo
                  tbody.bg-color-white
                    tr
                      td :
                      td Rango
                      td Produce una referencia a todas las celdas entre dos referencias.
                      td A1:A10
                    tr.bg-color-11
                      td ;
                      td Unión
                      td Combina múltiples referencias en una sola.
                      td SUMA(A1:A5;C1:C5)
    
    separador
    
    #t_4_2.titulo-segundo.color-acento-contenido(data-aos="flip-up")
      h2 4.2 Jerarquía de operadores 
    
    p.mb-5 Cuando una fórmula contiene varios operadores, Excel sigue un orden específico de cálculo, conocido como jerarquía u orden de precedencia. Comprender esta jerarquía es esencial, ya que una fórmula puede arrojar resultados incorrectos si se aplican los operadores en un orden no intencionado. A continuación, se presenta la jerarquía que Excel aplica al evaluar las fórmulas, de mayor a menor prioridad:

    .row.justify-content-center
      .col-lg-7  
        .titulo-sexto.color-acento-contenido
          h5 Tabla 8.
          span Jerarquía de operadores en Excel
        
        .tabla-a.color-acento-contenido.mb-5 
          table
            thead
              tr
                th.bg-color-2 Nivel
                th.bg-color-2 Tipo de operador
                th.bg-color-2 Símbolos o ejemplos
            tbody
              tr
                td 1
                td Operadores de referencia
                td :, ;
              tr.bg-color-11
                td 2
                td Negación
                td -1
              tr
                td 3
                td Porcentaje
                td %
              tr.bg-color-11
                td 4
                td Exponenciación
                td ^
              tr
                td 5
                td Multiplicación y división
                td *, /
              tr.bg-color-11
                td 6
                td Suma y resta
                td +, -
              tr
                td 7
                td Concatenación de texto
                td &
              tr.bg-color-11
                td 8
                td Comparación
                td 
                 |=, &lt;, &gt;, &lt;=, &gt;=, &lt;&gt;

    .row.justify-content-center
      .col-lg-8
        .bg-color-9.mb-5
          .px-4.px-md-5.py-4
            .row.align-items-center
              .col-lg-auto
                img(src="@/assets/curso/tema4/1.svg", style="max-width: 90px").mx-auto
              .col-lg
                h5 Regla práctica
                p La multiplicación y la división se realizan siempre antes que la suma y la resta, a menos que se usen paréntesis para cambiar el orden.
    
    h3.bg-color-14.d-inline.p-3.tarjeta Ejemplo ilustrativo

    .bg-full-width.bg-color-4
      .px-5.mb-5
        p.mt-5 Para comprender cómo influye la jerarquía de operadores en el resultado de una fórmula, observemos el siguiente caso: 
          span.etiqueta =5+2*3
        p.mb-5 Este cálculo no da como resultado 21. Según la jerarquía:
        .row.justify-content-center.mb-5
          .col-lg-4
            .bg-color-6.p-4
              ul.lista-ul--color.mb-0
                li.mb-0.d-flex
                  i.fas.fa-circle-check.bg-color-12
                  p.mb-0 Primero se realiza la multiplicación: 2*3 = 6.
                li.mb-0.d-flex
                  i.fas.fa-circle-check.bg-color-12
                  p.mb-0 Luego la suma: 5 + 6 = 11.
        p.mt-5 Por lo tanto, el resultado final es 11, no 21. Si se desea alterar ese orden y forzar que la suma se realice primero, se deben usar paréntesis: 
          span.etiqueta =5+2*3
        p.mb-5 Ahora Excel primero evalúa lo que está dentro del paréntesis: 5+2 = 7, y luego multiplica por 3, obteniendo el resultado 21.

        h3.bg-color-14.d-inline.p-3.tarjeta Actividad práctica
        p.mb-5.mt-5 Para reforzar el uso de operadores y comprender cómo funciona su jerarquía en Excel, se propone la siguiente actividad con ejercicios prácticos que combinan operadores aritméticos, de texto y el uso de paréntesis.

        .row.justify-content-center
          .col-lg-10
            .bg-color-8.mb-5(data-aos="fade-down")
              .row.justify-content-center.align-items-center
                .col-lg-auto.mb-3.mb-lg-0
                  figure
                    img(src='@/assets/curso/tema4/2.png', alt='')
                .col-lg
                  .p-4
                    h4 Tarea paso a paso
                    p Ejecute las siguientes acciones en Excel para aplicar los operadores aritméticos, de agrupación y de concatenación, y verificar cómo influyen en los resultados y en la construcción de expresiones.
                    ul.lista-ul--color.mb-0
                      li.mb-0.d-flex
                        i.fas.fa-circle-check.bg-color-12
                        p.mb-0 En una celda vacía, intente predecir el resultado de la siguiente fórmula y luego escríbala en Excel para verificar su respuesta: =10/2*5-(2+2)^2
                      li.mb-0.d-flex
                        i.fas.fa-circle-check.bg-color-12
                        p.mb-0 Cree una pequeña tabla con "Nombre" en A1 y "Apellido" en B1. En A2 escriba "Carlos" y en B2 "Rojas".
                      li.mb-0.d-flex
                        i.fas.fa-circle-check.bg-color-12
                        p.mb-0 En la celda C2, use el operador de concatenación para unir el nombre y el apellido, separados por un espacio, para que se muestre "Carlos Rojas".
    



</template>

<script>
export default {
  name: 'Tema4',
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
