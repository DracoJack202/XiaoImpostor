# 🕵️‍♂️ XiaoImpostor Bot

¡Bienvenido a **XiaoImpostor**! Un bot de Discord diseñado para jugar a un juego de engaño y deducción social (al estilo *Spyfall* o *El Espía*) directamente desde tus Mensajes Directos.

## 🎮 ¿Cómo se juega?
El objetivo del juego es simple: todos los jugadores reciben una **palabra secreta** por mensaje privado, excepto el/los **Impostor(es)**.
1. Los jugadores se reúnen en un canal de voz.
2. Por turnos, cada jugador dice una pista relacionada con la palabra secreta.
3. **Si eres Inocente:** Tu objetivo es dar una pista lo suficientemente clara para que los demás inocentes sepan que tú sabes la palabra, pero lo suficientemente vaga para que el Impostor no la adivine.
4. **Si eres el Impostor:** Tu objetivo es prestar atención, intentar deducir cuál es la palabra secreta y fingir que sabes de qué hablan para que no te descubran.

---

## 🛠️ Lista de Comandos

La mayoría de estos comandos están diseñados para usarse por **Mensaje Directo (MD)** con el bot para mantener el secreto del juego.

### 🏠 Comandos Básicos (Por MD)
* `/create` - Crea una nueva sala secreta y te da un código de 6 dígitos. Te conviertes en el Creador de la sala.
* `/join <código>` - Únete a la sala de un amigo usando su código.
* `/leave` - Sal de la sala en la que te encuentras.
* `/start` - *(Solo Creador)* Inicia la ronda. El bot repartirá las palabras y los roles de Impostor por privado a todos los jugadores.

### ⚙️ Gestión de la Sala (Comandos `/room`)
Estos comandos solo los puede usar el **Creador** de la sala por Mensaje Directo:
* `/room info` - Muestra la información de la sala: código, jugadores conectados, número de impostores y listas de palabras activas.
* `/room set_impostor <cantidad>` - Cambia cuántos impostores habrá en la siguiente ronda.
* `/room set_list <archivo> <peso>` - Añade o modifica la probabilidad (peso) de que salga una palabra de una lista específica. *(Ej: Peso 0 para desactivar, Peso 2 para que salga el doble de veces).*
* `/room kick <número>` - Expulsa a un jugador de la sala (puedes ver su número usando `/room info`).

### 🌐 Comandos de Servidor
* `/hola` - El bot saludará a todos en el canal del servidor. (Útil para comprobar si está encendido).

---

## 📁 Cómo añadir tus propias palabras

XiaoImpostor es totalmente personalizable. Puedes crear todas las categorías que quieras:

1. Ve a la carpeta donde está instalado el bot.
2. Crea un archivo de texto (`.txt`), por ejemplo: `videojuegos.txt`.
3. Escribe una palabra o frase por línea. No pongas comas ni comillas. Ejemplo:
'''
       Super Mario
       The Legend of Zelda
       Minecraft
'''
4. ¡Guarda el archivo! La próxima vez que uses `/room set_list` en Discord, el bot leerá automáticamente tu nuevo archivo y te dejará seleccionarlo.

---

## 🚀 Instalación y Arranque (Para el Host)

Si eres la persona que aloja el bot en su ordenador:

1. Asegúrate de tener Python 3 instalado.
2. Instala la librería de Discord ejecutando en tu terminal:
   ```bash
   pip install discord.py
   ```
3. Coloca tu Token de Discord en el archivo `bot.py` (¡Nunca compartas tu Token!).
4. Enciende el bot ejecutando:
   ```bash
   python3 bot.py
   ```
5. Espera a ver el mensaje `"Comandos de barra (/) sincronizados"` en la consola. ¡A jugar!
