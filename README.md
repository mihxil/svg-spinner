[![Maven Central](https://img.shields.io/maven-central/v/org.meeuw/svg-objects.svg?label=Maven%20Central)](https://search.maven.org/search?q=g:%22org.meeuw%22%20AND%20a:%22svg-objects%22)
[![Build Status](https://travis-ci.org/mihxil/svg-objects.svg?)](https://travis-ci.org/mihxil/svg-objects)
[![snapshots](https://img.shields.io/nexus/s/https/oss.sonatype.org/org.meeuw/svg-objects.svg)](https://oss.sonatype.org/content/repositories/staging/org/meeuw/svg-object/)
# svg-objects

# spinner

Use:  `/meeuw/spinner?<params>`
A parameterized SVG spinner in JSPX

If you have a servlet environment, than you can simply generate an SVG spinner using JSP. E.g. like this.

It can be parameterized and there is no need to generate these kind of things beforehand.

This version has the following parameters:
```jsp
  <c:set var="size" value="${empty param.size ? 64 : param.size}" />
  <!-- the square size of the spinner -->

  <c:set var="color" value="${empty param.color ? '#ed6d1c' : param.color}" />
  <!-- the fill color of the circles making up the spinner -->

  <c:set var="circles" value="${empty param.circles ? 7 : param.circles}" />
  <!-- The number of circles the spinner should be made up off -->

  <c:set var="steps" value="${empty param.steps ? 50 : param.steps}" />
  <!-- The number of steps used in one cycle of the animation -->

  <c:set var="dur" value="${empty param.dur ? '1500ms' : param.dur}" />
  <!-- The duration of one cycle of the animation -->
```
And the default then renders like so:
<img src="./spinner.svg">
