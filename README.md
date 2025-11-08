# Reeps - Gym Logger App

Aplicación móvil para registrar y seguir el progreso en el gimnasio, desarrollada con Flutter.

## Descripción

Reeps permite a los usuarios registrar entrenamientos (ejercicio, series, repeticiones, peso), visualizar el historial y obtener estadísticas gráficas del progreso. Está integrada con Firebase (Autenticación y Firestore) y usa un tema oscuro por defecto.

Este README ofrece instrucciones rápidas para configurar, ejecutar y contribuir al proyecto.

### Características principales

- Autenticación (Email/Password y Google Sign-In) usando Firebase Auth.
- Registro detallado de entrenamientos (sets, reps, peso, unidad).
- Cálculo de volumen (sets × reps × peso) para cada entrada.
- Biblioteca y búsqueda de ejercicios.
- Pantallas de detalle por ejercicio con historial.
- Estadísticas y gráficos de progreso (usa `fl_chart`).
- Tema centralizado (modo oscuro)

### Tecnologías

- Flutter (SDK Dart)
- Firebase Core / Auth / Firestore
- fl_chart, intl, provider, flutter_svg

### Requisitos

- Flutter SDK (compatible con SDK especificado en `pubspec.yaml`, p. ej. SDK >= 3.9.x).
- Android Studio / Xcode para emuladores o un dispositivo físico.
- Cuenta de Firebase para integrar autenticación y Firestore (ver sección de configuración).

## Instalación y Ejecución

1. Clona el repositorio:

```sh
git clone https://github.com/TheLucasBenji/reeps.git
cd reeps
```

2. Instala dependencias de Flutter:

```sh
flutter pub get
```

3. (Opcional) Instala íconos y splash si deseas regenerarlos localmente:

```sh
flutter pub run flutter_launcher_icons:main
flutter pub run flutter_native_splash:create
```

## Ejecutar la app

Para lanzar la app en un emulador o dispositivo conectado:

```bash
flutter run
```

Para compilar una APK de Android (release):

```bash
flutter build apk --release
```

Para compilar iOS (desde macOS con Xcode configurado):

```bash
flutter build ios --release
```

### Estructura relevante del proyecto

- `lib/` – Código fuente principal.
- `lib/screens/` – Pantallas como `home_screen.dart`, `add_workout_screen.dart`, etc.
- `lib/models/` – Modelos de datos (`exercise.dart`, `workout_record.dart`).
- `lib/config/theme.dart` – Tema centralizado de la app.
- `assets/` – Imágenes y recursos.


### Dependencias Clave
* **l_chart:** Para los gráficos de progreso en HomeScreen y StatisticsScreen.

* **intl:** Para formateo de fechas (visto en main.dart y add_workout_screen.dart).

* **provider:** Paquete de gestión de estado (disponible para uso futuro).

* **flutter_svg:** Para renderizar el logo en la pantalla de login.