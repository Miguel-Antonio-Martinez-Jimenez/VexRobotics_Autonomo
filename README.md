# Codigo Autonomo

1. Avanzar (forward)

    ```cpp bash
    // - Dirección: forward (adelante)
    // - Distancia: 50 (ajusta según tu robot)
    // - Unidades: inches (pulgadas)
    // - Velocidad: 50% (modifica si es muy rápido/lento)
    // - Bloqueante: true (espera a completar el movimiento)
    Drivetrain.driveFor(forward, 50, inches, 50, velocityUnits::pct, true);

2. Retroceder (reverse)

    ```cpp bash
    // - Dirección: reverse (atrás)
    // - Distancia: 30 (ajusta según tu robot)
    // - Unidades: inches (pulgadas)
    // - Velocidad: 70% (modifica si es muy rápido/lento)
    // - Bloqueante: true (espera a completar el movimiento)
    Drivetrain.driveFor(reverse, 30, inches, 70, velocityUnits::pct, true);

3. Giro a la Izquierda (left)

    ```cpp bash
    // - Dirección: left (izquierda)
    // - Ángulo: 90 grados
    // - Velocidad: 30% (giros suelen necesitar menos velocidad)
    Drivetrain.turnFor(left, 90, degrees, 30, velocityUnits::pct);

4. Giro a la Derecha (right)

    ```cpp bash
    // - Dirección: right (derecha)
    // - Ángulo: 90 grados
    // - Velocidad: 30% (giros suelen necesitar menos velocidad)
    Drivetrain.turnFor(right, 90, degrees, 30, velocityUnits::pct);

5. `NombreMotor.spinFor()` con Revoluciones

    ```cpp bash
    // - Dirección: forward
    // - Revoluciones: 0.30 (grados)
    // - Velocidad: 80% (modifica si es muy rápido/lento)
    // - Bloqueante: true (espera a completar el movimiento)
    NombreMotor.spinFor(forward, 0.30, rotationUnits::rev, 80, velocityUnits::pct, true);

6. `NombreMotor.spinFor()` con Tiempo

    ```cpp bash
    // - Dirección: forward
    // - Tiempo: 5 (duracion)
    // - Velocidad: 80% (modifica si es muy rápido/lento)
    // - Bloqueante: true (espera a completar el movimiento)
    NombreMotor.spinFor(forward, 5, timeUnits::sec, 80, velocityUnits::pct, true);

7. Estructura Genérica de `spinFor`
   
    ```cpp bash
    NombreMotor.spinFor(dirección, cantidad, unidades, velocidad, unidadesVelocidad, esperar?);

8. `NombreMotor.spin()` (Giro Continuo)

    ```cpp bash
    Brazo.spin(dirección, velocidad, unidades);
>[!IMPORTANT]
> Gira el motor indefinidamente en la dirección y velocidad especificadas hasta que se llame a `.stop().`
- Ejemplo:

    ```cpp bash
    Brazo.spin(forward, 60, percent);  // Gira al 60% hacia adelante
    wait(3, sec);                      // Espera 3 segundos
    Brazo.stop();                      // Detiene el motor
