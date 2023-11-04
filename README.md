# Aplicación de Principios y Arquitecturas de Sistemas Hipermedia
# Feature de destrucción progresiva
Por: Joe Cordero

Link del video en Loom: https://www.loom.com/share/791946b1b67548729b6f40427e8457cb?sid=19359a0b-86c5-44a0-98a4-e84eee5c0567

Este proyecto de Unity es un juego de disparos en el que el jugador puede destruir objetos, y como estos se pueden destruir progresivamente al momento que lo disparamos.

## Sistema de Destrucción de Objetos

El script `Shooted.cs` es responsable de manejar la lógica de destrucción de prefabs. Aquí está cómo funciona:

- Se define un valor de escala (`scaleFactor`) que se usa para reducir la escala del objeto con cada impacto, lo que simula la destrucción gradual.

- El contador `currentImpacts` registra cuántos impactos ha recibido el objeto. Cuando alcanza un valor máximo (`maxImpacts`), el objeto se destruye.

- Antes de destruir el objeto, se llama a la función `ReduceScale()` para reducir su tamaño gradualmente con cada impacto.
  
- `ReduceScale()` realiza el transform de la escala del objeto/prefab al que está asociado, a partir de ello nosotros podemos llamar este metodo en el momento que mejor nos convenga,
- según la lógica de nuestro juego.
