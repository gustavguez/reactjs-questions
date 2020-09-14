---- Preguntas - REACT ----
<>
  Qué es React?
  <>
    React es una librería Javascript focalizada en el desarrollo de interfaces de usuario.
    React es una librería desarrollada inicialmente por Facebook.
    Es software libre.
    Permite que las vistas se asocien con los datos.
    Si cambian los datos, también cambian las vistas.
    Permite la encapsulación del código en componentes.
    Es una librería y no un framework
    Sería la "V" en un framework "MVC",
  </>
</>
<>
  Qué es JSX?
  <>
    Es basicamente syntactic sugar para escribir la función React.createElement()
    Nos permite utilizar una sintaxis parecida a templates de HTML.
 </>
</>
<>
  Cómo creamos un componente en React?
  <>
    Hay dos tipos de componentes.
    Class y Function
  </>
</>
<>
  Cuándo usaríamos un componente de clase, en vez de uno función?
  <>
    Antes de React 16.8
    Si el componente necesita estado o acceder a los métodos de ciclo de vida y/o manejar estado necesitaremos un class component
    Sino, utilizaremos un function component. 
    Después de React 16.8
    Podemos manejar el ciclo de vida y el estado de un componente usando React hooks
  </>
</>
<>
  Qué es el estado de un componente?
  <>
    Es un objeto, que contiene información que puede cambiar a lo largo de la vida del componente.
  </>
</>
<>
  Qué son las props en React?
  <>
    Son parámetros a un componente.
    Son pasados hacia abajo en la jerarquía de componentes.
  </>
</>
<>
  Cuál es la diferencia entre el state y las props?
  <>
    Ambos son objetos de JS.
    El state es privado al componente, no es accesible desde otro componente.
    Las props son pasadas desde fuera, como si fueran parámetros de una función.
  </>
</>
<>
  Cómo se modifica el estado de un componente?
  <>
    this.setState({ key: '1' }) -> en los class component
  <>
</>
<>
  Por qué no deberíamos hacer update del estado de un componente directamente?
  <>
    Porque no se dispararía el re-render del componente.
    //Mal
    this.state.message = 'Hello world'
    //Correcto
    this.setState({ message: 'Hello World' }) -> o similar si usáramos hooks
  </>
</>
<>
  Cuál es la diferencia entre el manejo de eventos en HTML y en React?
  <>
    <button onclick='activateLasers()' />
    <button onClick={activateLasers} /> -> camel case, react usa synthetic events
  </>
</>
<>
  Qué son las props "key" y cuál es el beneficio de utilizarlas en arrays de elementos?
  <>
    Son una prop especial que hay que pasar a los elementos de un array cuando creamos una lista.
    Ayuda a React a identificar que items cambiaron, fueron agregados, o removidos.
    Se muestra un mensaje de Warning en la consola si esta prop no está presente.
  </>
</>
<>
  Qué es el DOM?
  <>
    DOM es una abreviatura de Document Objet Model.
    Es la jerarquía de objetos del navegador.
    Es una estructura jerárquica donde existen varios objetos y unos dependen de otros.
  </>
</>
<>
  Qué es el Virtual DOM?
  <>
    Es una representación en memoria del DOM Real.
    La representación de una UI es mantenida en memoria y se sincroniza con el DOM.
    Esa sincronización sucede entre que se llama a la función render, y se muestran los elementos en la pantalla
  </>
</>
<>
  Cuáles son las diferentes fases del ciclo de vida de un componente (class components)?
  <>
    Mounting: constructor(), render(), and componentDidMount()
    Updating: setState(), render(), componentDidUpdate(),
    Unmounting: componentWillUnmount()
  </>
</>
<>
  Cuál es el órden de los métodos en el ciclo de vida de montado (class components)?
  <>
    1. constructor()
    2. render()
    3. componentDidMount()
  </>
</>
<>
  Qué son los High-Order Components y para qué se utilizan?
  <>
    Un HOC es una funcion que toma un componente y retorna un nuevo componente.
    1. Reutilizar código
    2. Abstraer manipulación de estado
    3. Manipular las props
  </>
</>
<>
  Qué es una children prop?
  <>
    Children es una prop (prop.children) que nos permite pasar componentes como data a otros componentes
    Lo que está entre las etiquetas de apertura y cierre de un componente, será pasado como una prop children.
  </>
</>
<>
  Cómo escribimos un comentario en React?
    <>
     {/* <p> Comment in JSX </p> */}
     {`Welcome ${user}, let's play React`}
    </>
</>
<>
  Por qué utilizamos el atributo className en vez de class en React?
  <>
    Porque class es una palabra reservada en JS, y JSX es una extensión de JS.
  </>
</>
<>
  Qué son los fragmentos?
  <>
    Son un patrón utilizado para retornar múltiples elementos.
    No agregan nodos extras en el DOM.
  </>
</>
<>
  Por qué son mejores los fragmentos que los div?
  <>
    Son mas eficientes.
    Algunos mecanismos de CSS como Flexbox tienen una relación especial entre padres-hijos
    Añadir divs en el medio puede dificultar obtener el layout deseado.
    El inspector del DOM presentará menos elementos.
  </>
</>
<>
  Qué limitaciones tiene React?
  <>
    React es una librería, no un framework completo.
    Hay una curva de aprendizaje alta.
    La complejidad del código incrementa con los templates inline y JSX
    Demasiados componentes pequeños, pueden llevar a una sobre-ingeniería o demasiado boilerplate.
  </>
</>
<>
  Qué es CRA y cuáles son los beneficios de utilizarlo?
  <>
    create-react-app es una herramienta que permite crear y ejecutar rápidamente aplicaciones React.
    No necesita configuraciones previas.
    Incluye todo lo que necesitamos para construir una aplicación en React.
      1. soporte para React, JSX, ES6
      2. Extras del lenguaje para poder soportar cosas como el spread operator (...)
      3. Autoprefixed CSS, entonces no se necesitan cosas como -webkit- u otros prefijos.
      4. Un script para hacer builds de producción con todo el JS, CSS, etc.
  </>
</>
<>
  Cuál es el órden recomendado para escribir los métodos en un componente tipo clase?
  <>
    1. constructor()
    2. componentDidMount()
    3. componentDidUpdate()
    4. componentWillUnmount()
    5. click handlers or event handlers como onClickSubmit() or onChangeDescription()
    6. getter methods for render like getPuntaje()
    7. render()
  </>
</>
---- Preguntas - REDUX ----
<>
  Qué es Flux?
  <>
    Flux reemplaza formas más tradicionales de manejo de datos, como el patrón MVC
    No es un framework o una librería, sino un tipo de arquitectura que complementa a React,
    y el concepto de Flujo Unidireccional de Datos.
  </>
</>
<>
  Qué es Redux?
  <>
    Redux está basado en el patrón de Flux.
    Es una implementación de Flux para lograr manejo de estado.
    Puede ser utilizado con React o con otras librerías.
  </>
</>
<>
  Cuáles son los principios básicos de Redux?
  <>
    1. Única fuente de la verdad: El estado de toda la aplicación está guardado en un objeto dentro de una única store.
    2. El estado es read-only. La única forma de cambiar el estado es emitiendo una acción.
       Esto nos asegura que ni la vista ni algún efecto secundario va a cambiar el estado directamente.
    3. Los cambios están implementados con funciones puras.
       Los Reducers son funciones puras que toman el estado anterior y una acción como parámetros. Y retornan un nuevo estado.
  </>
</>
<>
  Cuál es la diferencia entre mapStateToProps() y mapDispatchToProps()? -> en el curso usamos los hooks useSelector y useDispatch que tienen un propósito similar
  <>
    mapStateToProps() ayuda al componente a obtener el estado actualizado.
    mapDispatchToProps() ayuda al componente a disparar una acción sobre un evento (dispatchear una acción)
  </>
</>
<>
  Puedo dispatchear una action en un reducer?
  <>
    Es un anti-patrón.
    El reducer no debería tener efectos secundarios.
  </>
</>
<>
  Qué es Redux Thunk?
  <>
    Redux Thunk es un middleware que permite crear actions como funciones en vez de como objetos.
    Los thunks pueden ser utilizados para demorar el dispatcheo de una acción.
    También para dispatchear acciones solamente dadas determinadas condiciones.
  </>
</>
