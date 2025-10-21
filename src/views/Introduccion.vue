<template lang="pug">
.curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido(data-aos="flip-up")
      .titulo-principal__numero
        span
          i.fas.fa-info
      h1 Introducción
    
    p.mb-5 En el entorno laboral actual, la capacidad de gestionar, analizar y presentar información de manera eficiente es una habilidad transversal de inmenso valor que todas las empresas al momento de contratar nuevo personal tienen en cuenta. Microsoft Excel se ha consolidado como la herramienta líder a nivel mundial para este tipo de tareas, transformándose en un pilar para la toma de decisiones en áreas tan diversas como finanzas, marketing, ingeniería y gestión de recursos humanos.

    .bloque-texto-g.color-secundario.p-3.p-sm-4.p-md-5.mb-5
      .bloque-texto-g__img(
        :style="{'background-image': `url(${require('@/assets/curso/intro/1.png')})`}"
      )(data-aos="zoom-in")
      .bloque-texto-g__texto.p-4
        p.mb-0 Es por eso por lo que, el dominio de Excel va más allá de la simple introducción de datos en una cuadrícula. Su verdadero poder reside en la capacidad de automatizar cálculos, manipular grandes volúmenes de información y generar reportes significativos a través del uso de fórmulas y funciones.
    
    .bg-color-1.mb-5
      .p-4
        .row.align-items-center
          .col-lg-auto.order-2
            img(src="@/assets/curso/intro/2.svg", style="max-width: 90px").mx-auto
          .col-lg.order-1.mb-3.mb-lg-0
            p.mb-0 Este componente formativo se ha diseñado para guiarlo, en el desarrollo de las competencias necesarias para estructurar datos en hojas de cálculo utilizando fórmulas, funciones y los requerimientos del entorno. Al finalizar, usted no solo comprenderá la anatomía de una hoja de cálculo, sino que también será capaz de construir fórmulas personalizadas y robustas, utilizar funciones predeterminadas y presentar sus datos de una manera clara y profesional, sentando las bases para análisis más complejos en el futuro.

</template>

<script>
export default {
  name: 'Introduccion',
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
