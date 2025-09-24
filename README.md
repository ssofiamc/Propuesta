La navegación en una aplicación Ionic con Angular utiliza el enrutador de Angular y el sistema de enrutamiento de Ionic para gestionar las transiciones entre páginas, similar a otras aplicaciones web complejas, pero con un sistema de pila de historial interno que maneja 
los componentes de forma más eficiente para dispositivos móviles. Esto permite crear experiencias de usuario similares a las de aplicaciones nativas, con pilas de navegación individuales para pestañas y un manejo de la interfaz que mantiene las páginas cargadas pero
ocultas para acelerar las transiciones y la reutilización de componentes. 


Componentes y conceptos clave
Enrutador de Angular y enrutador de Ionic: El enrutador de Ionic extiende el enrutador de Angular, permitiendo su uso conjunto. El enrutador de Ionic maneja el estado de la pila y las animaciones de páginas, mientras que el de Angular se enfoca en la navegación basada 
en URL. 
Pila de historial (Stack): A diferencia de las bibliotecas web tradicionales, Ionic mantiene una pila de historial interna para cada sección de la aplicación. Esto significa que las páginas no se eliminan del DOM, sino que se vuelven invisibles y se pueden reutilizar 
para un mejor rendimiento y una experiencia de usuario más fluida. 
Componente ionic-nav: Este componente es útil para crear subnavegaciones dentro de componentes o modales sin afectar la URL principal de la aplicación. Permite "empujar" (push) nuevos componentes a una pila o volver a la raíz, ideal para la navegación dentro de un modal 
que no requiere una nueva ruta en el navegador. 
Pestañas con pilas individuales: Cada pestaña en una aplicación Ionic tiene su propia pila de navegación independiente, lo que permite navegar hacia adelante y hacia atrás dentro de cada pestaña sin afectar a las otras. 


Cómo funciona la navegación
Configuración de rutas: Se definen rutas usando el módulo de enrutamiento de Angular, donde cada ruta apunta a un componente o a un módulo cargado de forma diferida (lazy loading). 
Navegación a una página: Para moverse entre páginas, se utiliza el enrutador de Angular para navegar a una URL específica, lo que carga el componente asociado y lo empuja a la pila de navegación. 
Navegación en pestañas: Al hacer clic en una pestaña, se carga una pila de navegación individual. Al ir a una nueva vista dentro de la pestaña, se utiliza el componente ion-nav para enviar el nuevo componente a la pila, que luego se vuelve visible. 
Regresar a una página: Se puede utilizar la función para regresar a la página anterior o a la página raíz, aprovechando la pila de historial para mostrar el componente anterior. 


Ventajas de la navegación en Ionic y Angular
Experiencia de usuario similar a la nativa: El manejo de pilas de historial y la reutilización de componentes hacen que las transiciones sean más rápidas y fluidas, emulando la sensación de una aplicación móvil nativa. 
Mayor capacidad de respuesta: Al mantener los componentes en el DOM, Ionic puede reutilizar y animar páginas ya cargadas, lo que mejora la respuesta de la aplicación. 
Flexibilidad: La integración del enrutador de Angular con las funcionalidades de Ionic proporciona una solución de navegación robusta y flexible para aplicaciones complejas. 

Referencias
Ionic Framework (s.f.) Ionic Docs. https://ionicframework.com/docs/angular/navigation#:~:text=C%C3%B3mo%20funcionan%20las%20pesta%C3%B1as%20en,sobre%20algunas%20de%20estas%20diferencias.
