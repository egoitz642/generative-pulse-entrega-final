# GenerativePulse

GenerativePulse es una app movil construida con Capacitor, Vite, Vanilla JS y p5.js que transforma un temporizador de enfoque tipo Pomodoro en una experiencia visual interactiva. El proyecto combina una animacion generativa que responde al estado de la sesion, persistencia local de configuracion y una integracion con API externa para mostrar consejos dinamicos.

Este README fue reorganizado siguiendo la linea sugerida en el articulo "The Ultimate Guide to Writing a Great README.md for Your Project": descripcion clara, tabla de contenidos, instalacion, uso, funcionalidades, capturas, documentacion complementaria y licencia.

## Tabla de contenidos

* [Descripcion del proyecto](#descripcion-del-proyecto)
* [Caracteristicas principales](#caracteristicas-principales)
* [Tecnologias utilizadas](#tecnologias-utilizadas)
* [Instalacion](#instalacion)
* [Uso](#uso)
* [Estructura principal](#estructura-principal)
* [Capturas](#capturas)
* [Proceso creativo](#proceso-creativo)
* [Documentacion de entrega](#documentacion-de-entrega)
* [Fuentes](#fuentes)
* [Contribucion](#contribucion)
* [Licencia](#licencia)

## Descripcion del proyecto

La app propone una version expandida del Pomodoro tradicional:

* El canvas generativo cambia segun el avance del tiempo y el modo activo.
* La vibracion nativa avisa cuando termina un ciclo de foco o descanso.
* La configuracion del usuario se guarda localmente.
* Un consejo externo puede actualizarse segun un tema elegido por el usuario.
* El consejo puede mostrarse traducido al español para mejorar la experiencia.

## Caracteristicas principales

* Temporizador con modos de foco y descanso.
* Visual generativa en p5.js sincronizada con el estado de la sesion.
* Persistencia local con `@capacitor/preferences`.
* Vibracion nativa al completar un ciclo con `@capacitor/haptics`.
* Consulta externa configurable sin API key.
* Seleccion de tema sugerido o tema personalizado para pedir consejos.
* Traduccion opcional del consejo al español.
* Funcionamiento degradado en navegador cuando una capacidad nativa no esta disponible.

## Tecnologias utilizadas

* Vite
* Vanilla JavaScript
* Capacitor
* `@capacitor/android`
* `@capacitor/haptics`
* `@capacitor/preferences`
* p5.js

## Instalacion

### Requisitos previos

* Node.js
* npm
* Android Studio si se desea probar la app nativa

### Pasos

1. Clonar el repositorio:

```bash
git clone <URL\_DEL\_REPOSITORIO>
cd generative-pulse-entrega-final
```

2. Instalar dependencias:

```bash
npm install
```

3. Ejecutar el entorno web de desarrollo:

```bash
npm run dev
```

## Uso

### En navegador

```bash
npm run dev
```

Esto abre la version web para probar:

* El temporizador de foco y descanso.
* La animacion generativa reactiva.
* La configuracion de minutos, API y tema del consejo.
* La traduccion opcional del contenido externo.

### Build de produccion

```bash
npm run build
```

### Sincronizar y abrir Android

```bash
npm run android:sync
npm run android:open
```

### Flujo completo para entrega o revision en Android Studio

```bash
npm run android:run
```

## Estructura principal

* `src/main.js`: interfaz, logica del temporizador, preferencias, consulta externa y traduccion.
* `src/sketch.js`: canvas generativo implementado en p5.js.
* `src/style.css`: estilos responsivos para web y vista movil.
* `src/assets/`: capturas e imagenes de apoyo para la documentacion.
* `android/`: proyecto nativo generado por Capacitor.

## Capturas

Las siguientes imagenes documentan el comportamiento y la evolucion de la app:

!\[Pantalla inicial](src/assets/imageInicial.png)
!\[Modo foco](src/assets/imageModoFoco.png)
!\[Animacion en foco](src/assets/imageModoFocoAnimacion.png)
!\[Modo descanso](src/assets/imageModoDescanso.png)
!\[Consulta a API externa](src/assets/imageActDatoConAPIExterna.png)

Capturas adicionales de la segunda entrega:

* `src/assets/segundaEntrega/imageEstadoBaseAntesTema.png`
* `src/assets/segundaEntrega/imageTemaConsejoSelect1.png`
* `src/assets/segundaEntrega/imageOtroTemaPersonalizado.png`
* `src/assets/segundaEntrega/imageConsejoPersonalizado1.png`
* `src/assets/segundaEntrega/imageConsejoTraducidoEspanol2.png`

## Proceso creativo

La propuesta parte de un temporizador base y lo transforma en una experiencia con identidad visual propia. La decision central fue que el canvas no fuera decorativo, sino una representacion del ritmo de la sesion.

Lineas de diseno del proyecto:

* En foco, la animacion refuerza energia, avance e intensidad.
* En descanso, el comportamiento visual baja el ritmo para sugerir pausa.
* La vibracion se eligio como componente nativo util porque notifica cambios sin depender de sonido.
* La integracion externa agrega variacion y personalizacion a cada sesion.

## Documentacion de entrega

* `PROCESO\_DESARROLLO.md`
* `BOCETOS\_Y\_CAPTURAS.md`
* `PRUEBAS\_Y\_MEJORAS.md`
* `NOTA\_DISPOSITIVO\_ANDROID.md`
* `PUBLICACION\_WEB.md`
* `FUENTES\_Y\_USO\_IA.md`
* `LICENSE`

El documento `BOCETOS\_Y\_CAPTURAS.md` concentra la evidencia visual del proyecto y referencia las capturas incluidas en `src/assets/`.

## Fuentes

* Capacitor Docs: https://capacitorjs.com/docs
* Vite Guide: https://vite.dev/guide/
* p5.js Reference: https://p5js.org/reference/
* Advice Slip API: https://api.adviceslip.com/
* Articulo de referencia para la mejora del README: https://medium.com/@kc\_clintone/the-ultimate-guide-to-writing-a-great-readme-md-for-your-project-3d49c2023357

## Contribucion

Este proyecto fue preparado como entrega academica en la UOC, pero si se quisiera extender, una forma simple de contribuir seria:

1. Crear una rama nueva para la mejora.
2. Implementar el cambio.
3. Probar el flujo web y Android.
4. Documentar el ajuste realizado.

## Licencia

Este proyecto se distribuye bajo la [MIT License](LICENSE).

