# Angular: La Guía en Español

> La guía de Angular en español. Cubre Angular 17–21 desde los fundamentos hasta arquitecturas de nivel enterprise, con Signals, NgRx, SSR, micro-frontends y todo lo nuevo en Angular 20 y 21.

---

## ¿Qué es esta guía?

Esta guía está escrita para desarrolladores hispanohablantes que quieren dominar Angular de verdad - no solo aprender la sintaxis, sino entender el *por qué* detrás de cada decisión de diseño del framework. Cada concepto se explica como lo haría un senior a un colega: directo, honesto y con ejemplos que resuelven problemas reales.

No es un tutorial de "hola mundo" ni una traducción de la documentación oficial. Es una guía de referencia progresiva que construye conocimiento de forma acumulativa, partiendo de los fundamentos y llegando a patrones avanzados de arquitectura, rendimiento y despliegue en producción.

**Todo el código es Angular 17+** con TypeScript estricto, componentes standalone y la nueva sintaxis de control de flujo (`@if`, `@for`, `@defer`). Los capítulos finales cubren las novedades de **Angular 20 y 21**.

---

## Requisitos previos

- Conocimientos básicos de **HTML y CSS**
- Familiaridad con **JavaScript moderno** (ES2020+, async/await, módulos)
- Conocimiento básico de **TypeScript** (tipos, interfaces, clases, generics)
- No se requiere experiencia previa con Angular ni con otros frameworks

---

## Versiones cubiertas

| Versión | Fecha | Lo que se cubre en esta guía |
|---|---|---|
| Angular 15 | Nov 2022 | Guards y resolvers funcionales, interceptores funcionales |
| Angular 16 | May 2023 | Signals (developer preview), `takeUntilDestroyed` |
| Angular 17 | Nov 2023 | Standalone default, `@if/@for/@defer`, Signals estables |
| Angular 18 | May 2024 | `linkedSignal`, `resource` (experimental) |
| Angular 19 | Nov 2024 | `httpResource`, hydratación incremental (experimental) |
| Angular 20 | May 2025 | `@let`, signal queries, Zoneless dev preview, SSR por ruta |
| Angular 21 | Nov 2025 | Zoneless estable, Signal Forms dev preview, `@angular/build` |

---

## Cómo navegar la guía

La guía está organizada en **15 partes temáticas** con **36 capítulos** y **144 archivos**. Cada archivo cubre una parte de un capítulo (entre 3 y 7 páginas de contenido denso).

**Si eres principiante:** lee en orden desde la Parte I. Cada capítulo asume el conocimiento de los anteriores.

**Si tienes experiencia con Angular:** puedes ir directamente a la parte que necesitas. Los capítulos avanzados (XI en adelante) son relativamente autónomos.

**Como referencia:** usa la tabla de contenidos abajo para ir directamente al tema específico.

---

## Tabla de contenidos completa

### PARTE I - Primeros Pasos con Angular
*Capítulos 1–2 · 8 archivos*

Cubre la historia del framework, el ecosistema de herramientas, la estructura de un proyecto y el proceso de arranque. Ideal para quien nunca ha tocado Angular.

| Archivo | Título | Descripción breve |
|---|---|---|
| [docs/chapter01/part1.md](docs/chapter01/part1.md) | Historia, versiones y el renacimiento de Angular | De AngularJS a Angular 2+, el ciclo de releases semver, la era Ivy y Standalone |
| [docs/chapter01/part2.md](docs/chapter01/part2.md) | Angular vs React vs Vue: cuándo elegir cada uno | Comparativa sin favoritismos; casos donde Angular brilla (enterprise, tipado estricto) |
| [docs/chapter01/part3.md](docs/chapter01/part3.md) | Instalación de Node, Angular CLI y VS Code | Setup completo del entorno con extensiones recomendadas y diagrama del toolchain |
| [docs/chapter01/part4.md](docs/chapter01/part4.md) | Tu primera aplicación: ng new al primer ng serve | Crear un proyecto, explorar la estructura y hacer el primer cambio con live reload |
| [docs/chapter02/part1.md](docs/chapter02/part1.md) | Visión general: módulos, componentes, servicios | Diagrama de cómo se relacionan los bloques principales de Angular |
| [docs/chapter02/part2.md](docs/chapter02/part2.md) | Angular CLI a fondo: comandos esenciales y schematics | `ng generate`, `ng build`, `ng test`, `ng lint`, flags útiles como `--dry-run` |
| [docs/chapter02/part3.md](docs/chapter02/part3.md) | Estructura de carpetas y convenciones de proyecto | Feature-based structure, barrel exports, convenciones de nombres kebab-case/PascalCase |
| [docs/chapter02/part4.md](docs/chapter02/part4.md) | El proceso de arranque: main.ts, AppModule y bootstrap | `bootstrapApplication()`, `APP_INITIALIZER`, `provideRouter`, `provideHttpClient` |

---

### PARTE II - Componentes: El Alma de Angular
*Capítulos 3–4 · 8 archivos*

Todo lo que necesitas saber sobre componentes: desde la anatomía básica hasta técnicas avanzadas de proyección de contenido y carga diferida de UI.

| Archivo | Título | Descripción breve |
|---|---|---|
| [docs/chapter03/part1.md](docs/chapter03/part1.md) | Anatomía de un componente: clase, decorador y template | Las tres partes de un componente, el decorador `@Component` y sus propiedades |
| [docs/chapter03/part2.md](docs/chapter03/part2.md) | Ciclo de vida: OnInit, OnChanges, OnDestroy y los demás | Los 8 hooks en orden de ejecución con casos de uso y diagrama Mermaid |
| [docs/chapter03/part3.md](docs/chapter03/part3.md) | Comunicación con @Input y @Output | `@Input()` con alias y transformaciones, `@Output()` con `EventEmitter`, patrón padre-hijo |
| [docs/chapter03/part4.md](docs/chapter03/part4.md) | Estilos en componentes: encapsulación y ViewEncapsulation | `Emulated`, `None`, `ShadowDom`, `:host`, variables CSS, theming |
| [docs/chapter04/part1.md](docs/chapter04/part1.md) | ViewChild, ViewChildren y ElementRef | `@ViewChild` con tipos de referencia, `QueryList`, `static: true` vs `false` |
| [docs/chapter04/part2.md](docs/chapter04/part2.md) | ng-content: proyección de contenido simple y múltiple | `<ng-content>`, proyección con `select`, `ContentChild`, componente card reutilizable |
| [docs/chapter04/part3.md](docs/chapter04/part3.md) | Componentes Standalone: el futuro de Angular | `standalone: true`, `imports` en el decorador, bootstrap sin NgModule |
| [docs/chapter04/part4.md](docs/chapter04/part4.md) | Deferrable Views con @defer: carga diferida de UI | `@defer`, `@loading`, `@error`, triggers de viewport/interacción/timer, impacto en LCP |

---

### PARTE III - Templates y Directivas
*Capítulos 5–6 · 8 archivos*

Data binding en todas sus formas, la nueva sintaxis de control de flujo y cómo crear directivas personalizadas de atributo y estructurales.

| Archivo | Título | Descripción breve |
|---|---|---|
| [docs/chapter05/part1.md](docs/chapter05/part1.md) | Interpolación y Property Binding | `{{ }}`, `[prop]`, attribute vs property binding, `[class.x]`, `[style.y]` |
| [docs/chapter05/part2.md](docs/chapter05/part2.md) | Event Binding y Two-way Binding | `(evento)`, `$event`, `[(ngModel)]`, two-way con Signal inputs |
| [docs/chapter05/part3.md](docs/chapter05/part3.md) | Template Reference Variables y @ViewChild | `#refVar` en templates, pasar refs a métodos, diferencias entre enfoques |
| [docs/chapter05/part4.md](docs/chapter05/part4.md) | Nueva sintaxis de control de flujo: @if, @for, @switch | `@if/@else if/@else`, `@for` con `track` obligatorio, `@switch`, diferencias con `*ngIf` legacy |
| [docs/chapter06/part1.md](docs/chapter06/part1.md) | Directivas estructurales built-in: ngIf, ngFor, ngSwitch | `*ngIf`, `ngIfThen`, `*ngFor` con `index/first/last`, cuándo migrar a nueva sintaxis |
| [docs/chapter06/part2.md](docs/chapter06/part2.md) | Directivas de atributo built-in: ngClass, ngStyle | `[ngClass]` con objeto/array/string, `[ngStyle]`, diferencias con bindings directos |
| [docs/chapter06/part3.md](docs/chapter06/part3.md) | Creando directivas de atributo personalizadas | `@Directive`, `Renderer2`, directiva `appResaltado` con `@HostListener` |
| [docs/chapter06/part4.md](docs/chapter06/part4.md) | HostListener, HostBinding y directivas estructurales propias | `@HostListener`, `@HostBinding`, directiva estructural con `TemplateRef` y `ViewContainerRef` |

---

### PARTE IV - Pipes: Transformando Datos
*Capítulo 7 · 4 archivos*

Los pipes built-in de Angular, cómo encadenarlos y parametrizarlos, y cómo crear pipes personalizados con control total del rendimiento.

| Archivo | Título | Descripción breve |
|---|---|---|
| [docs/chapter07/part1.md](docs/chapter07/part1.md) | Pipes built-in: date, currency, number, json, async | `DatePipe`, `CurrencyPipe`, `DecimalPipe`, `AsyncPipe` con Observable y Promise, `LOCALE_ID` |
| [docs/chapter07/part2.md](docs/chapter07/part2.md) | Parámetros de pipes y encadenamiento | Sintaxis `\| pipe:param1:param2`, encadenamiento múltiple, orden de evaluación |
| [docs/chapter07/part3.md](docs/chapter07/part3.md) | Creando pipes personalizados con PipeTransform | `@Pipe({ name, standalone, pure })`, ejemplo `filtrarPor` y `truncarTexto` |
| [docs/chapter07/part4.md](docs/chapter07/part4.md) | Pipes puros vs impuros: impacto en rendimiento | Qué es un pipe puro, cuándo necesitas `pure: false` y el costo, alternativas |

---

### PARTE V - Servicios e Inyección de Dependencias
*Capítulos 8–9 · 8 archivos*

La arquitectura de capas de Angular, el sistema de DI, la jerarquía de inyectores y la migración completa del mundo NgModules al mundo Standalone.

| Archivo | Título | Descripción breve |
|---|---|---|
| [docs/chapter08/part1.md](docs/chapter08/part1.md) | ¿Qué es un servicio? Responsabilidad única y separación de capas | Problema que resuelven, diagrama de capas (presentación / lógica / datos) |
| [docs/chapter08/part2.md](docs/chapter08/part2.md) | Creando e inyectando servicios | `@Injectable({ providedIn: 'root' })`, inyección por constructor vs `inject()` |
| [docs/chapter08/part3.md](docs/chapter08/part3.md) | Inyección de Dependencias: el sistema DI de Angular | Tokens de inyección, `InjectionToken<T>`, `@Inject()`, `inject()` en funciones puras |
| [docs/chapter08/part4.md](docs/chapter08/part4.md) | Jerarquía de inyectores: root, módulo y componente | Árbol de inyectores, resolución de dependencias, instancias separadas por componente |
| [docs/chapter09/part1.md](docs/chapter09/part1.md) | NgModules: declarations, imports, exports, providers | Anatomía de `@NgModule`, qué va en cada array, errores comunes |
| [docs/chapter09/part2.md](docs/chapter09/part2.md) | Módulo Core, Shared y de funcionalidad | Patrón de tres tipos de módulos, `forRoot()` para evitar importar CoreModule dos veces |
| [docs/chapter09/part3.md](docs/chapter09/part3.md) | El mundo Standalone: componentes, directivas y pipes sin módulo | `standalone: true`, imports en el decorador, ventajas en tree-shaking, `importProvidersFrom` |
| [docs/chapter09/part4.md](docs/chapter09/part4.md) | Guía de migración: de NgModules a Standalone | Comando automático `ng generate @angular/core:standalone`, fases, compatibilidad híbrida |

---

### PARTE VI - Navegación y Routing
*Capítulos 10–11 · 8 archivos*

Configuración del router, navegación programática, rutas dinámicas, lazy loading, guards funcionales y estrategias de preloading.

| Archivo | Título | Descripción breve |
|---|---|---|
| [docs/chapter10/part1.md](docs/chapter10/part1.md) | Configuración del Router: provideRouter y rutas básicas | `provideRouter(routes)`, objeto de ruta, `redirectTo`, `pathMatch`, ruta wildcard `**` |
| [docs/chapter10/part2.md](docs/chapter10/part2.md) | RouterLink, RouterOutlet y navegación programática | `<router-outlet>`, `[routerLink]`, `routerLinkActive`, `Router.navigate()` |
| [docs/chapter10/part3.md](docs/chapter10/part3.md) | Rutas con parámetros :id y Query Params | `paramMap` como Observable, `queryParams`, `fragment`, lectura con `inject(ActivatedRoute)` |
| [docs/chapter10/part4.md](docs/chapter10/part4.md) | Rutas hijas (Child Routes) y outlets secundarios | `children` en rutas, `<router-outlet>` anidado, outlets con nombre |
| [docs/chapter11/part1.md](docs/chapter11/part1.md) | Lazy Loading: cargando módulos y componentes bajo demanda | `loadComponent`, `loadChildren`, impacto en bundle size, verificar chunks en DevTools |
| [docs/chapter11/part2.md](docs/chapter11/part2.md) | Guards funcionales: canActivate, canDeactivate, canMatch | Guards como funciones (Angular 14+), `inject()` dentro del guard, redirigir desde guard |
| [docs/chapter11/part3.md](docs/chapter11/part3.md) | Resolvers: precargando datos antes de navegar | `ResolveFn<T>`, acceder a datos resueltos, cuándo NO usar resolvers, alternativa con Signals |
| [docs/chapter11/part4.md](docs/chapter11/part4.md) | Estrategias de preloading: PreloadAllModules y personalizadas | `PreloadAllModules`, estrategia personalizada, preloading selectivo, `QuicklinkStrategy` |

---

### PARTE VII - Formularios
*Capítulos 12–13 · 8 archivos*

Los dos enfoques de formularios en Angular: template-driven para casos simples y reactive forms para validación compleja, dinámismo y control total.

| Archivo | Título | Descripción breve |
|---|---|---|
| [docs/chapter12/part1.md](docs/chapter12/part1.md) | Fundamentos: ngModel, ngForm y FormsModule | `[(ngModel)]`, `ngForm`, `form.valid`, `form.value`, submit con `(ngSubmit)` |
| [docs/chapter12/part2.md](docs/chapter12/part2.md) | Validación con atributos HTML y directivas de Angular | `required`, `minlength`, `pattern`, clases CSS `ng-valid/ng-invalid/ng-touched` |
| [docs/chapter12/part3.md](docs/chapter12/part3.md) | Mensajes de error y clases CSS de estado | Estrategias para mostrar errores, componente de campo reutilizable, reset de formulario |
| [docs/chapter12/part4.md](docs/chapter12/part4.md) | Formularios anidados con ngModelGroup | `ngModelGroup` para agrupar campos, acceder a subgrupos, validación de grupo |
| [docs/chapter13/part1.md](docs/chapter13/part1.md) | FormControl, FormGroup y FormBuilder | `new FormControl<T>()`, `FormBuilder.group()`, `FormBuilder.nonNullable`, tipado genérico |
| [docs/chapter13/part2.md](docs/chapter13/part2.md) | Validators síncronos y asíncronos built-in | `Validators.required/email/min/max/pattern`, `AsyncValidatorFn` con `debounceTime` |
| [docs/chapter13/part3.md](docs/chapter13/part3.md) | FormArray: listas dinámicas de controles | `FormArray`, `push()`, `removeAt()`, tipado genérico, validación del array completo |
| [docs/chapter13/part4.md](docs/chapter13/part4.md) | Validadores personalizados y cross-field validation | `ValidatorFn`, validación de contraseñas iguales, `AsyncValidatorFn` que consulta una API |

---

### PARTE VIII - Comunicación HTTP
*Capítulos 14–15 · 8 archivos*

`HttpClient` con tipado genérico, manejo de errores, interceptores funcionales para autenticación, loading global y caché con RxJS.

| Archivo | Título | Descripción breve |
|---|---|---|
| [docs/chapter14/part1.md](docs/chapter14/part1.md) | Configuración con provideHttpClient y primera petición GET | `provideHttpClient()`, inyectar `HttpClient`, primer `get<T>()`, async pipe |
| [docs/chapter14/part2.md](docs/chapter14/part2.md) | POST, PUT, PATCH, DELETE con tipado genérico | Métodos HTTP con body tipado, interfaces de respuesta, opciones por request |
| [docs/chapter14/part3.md](docs/chapter14/part3.md) | Manejo de errores con catchError y tipado de respuestas | `HttpErrorResponse`, `catchError`, errores de cliente vs servidor, estrategias de notificación |
| [docs/chapter14/part4.md](docs/chapter14/part4.md) | Headers, params, HttpContext y opciones avanzadas | `HttpHeaders`, `HttpParams`, `observe: 'response'`, `reportProgress`, `HttpContext` |
| [docs/chapter15/part1.md](docs/chapter15/part1.md) | Interceptores funcionales (Angular 15+): concepto y estructura | `HttpInterceptorFn`, `request.clone()`, `withInterceptors([])`, orden de ejecución |
| [docs/chapter15/part2.md](docs/chapter15/part2.md) | Interceptor de autenticación: adjuntando JWT automáticamente | Leer token desde servicio, `Authorization: Bearer`, excluir URLs públicas, manejar 401 |
| [docs/chapter15/part3.md](docs/chapter15/part3.md) | Interceptor de loading global y manejo centralizado de errores | Contador con Signal, spinner global, interceptor de errores con toast, `finalize()` |
| [docs/chapter15/part4.md](docs/chapter15/part4.md) | Estrategias de caché HTTP y retry con RxJS | `shareReplay(1)`, caché con `Map`, `retry(3)`, backoff exponencial con `retryWhen` |

---

### PARTE IX - Programación Reactiva con RxJS
*Capítulos 16–18 · 12 archivos*

RxJS de cero a avanzado: Observables, Subjects, operadores de transformación/filtrado/combinación, patrones reactivos en servicios y marble testing.

| Archivo | Título | Descripción breve |
|---|---|---|
| [docs/chapter16/part1.md](docs/chapter16/part1.md) | ¿Qué es la programación reactiva? Observables vs Promesas | Push vs pull, lazy vs eager, unicast vs multicast, diagrama comparativo |
| [docs/chapter16/part2.md](docs/chapter16/part2.md) | Observable, Observer, Subscription y el contrato reactivo | Anatomía del Observable, `next/error/complete`, cold vs hot, `unsubscribe()` |
| [docs/chapter16/part3.md](docs/chapter16/part3.md) | Subject, BehaviorSubject, ReplaySubject y AsyncSubject | Cuándo usar cada tipo de Subject, comparativa con diagrama Mermaid |
| [docs/chapter16/part4.md](docs/chapter16/part4.md) | Creadores: of, from, interval, timer, fromEvent | `of`, `from`, `interval`, `timer`, `fromEvent`, `EMPTY`, `NEVER`, `throwError` |
| [docs/chapter17/part1.md](docs/chapter17/part1.md) | Transformación: map, switchMap, mergeMap, concatMap, exhaustMap | Diferencias críticas entre los cuatro operadores de aplanamiento con ejemplos reales |
| [docs/chapter17/part2.md](docs/chapter17/part2.md) | Filtrado: filter, take, first, debounceTime, distinctUntilChanged | Buscador con `debounceTime(300)` + `distinctUntilChanged` + `switchMap` |
| [docs/chapter17/part3.md](docs/chapter17/part3.md) | Combinación: combineLatest, forkJoin, zip, withLatestFrom | Peticiones paralelas, combinar filtros reactivos, sincronización de streams |
| [docs/chapter17/part4.md](docs/chapter17/part4.md) | Manejo de errores: catchError, retry, retryWhen, throwError | `catchError` con alternativa o re-lanzamiento, backoff exponencial, `finalize` |
| [docs/chapter18/part1.md](docs/chapter18/part1.md) | Patrones reactivos en servicios Angular | State service con `BehaviorSubject`, `asObservable()`, `shareReplay(1)` |
| [docs/chapter18/part2.md](docs/chapter18/part2.md) | Evitando memory leaks: takeUntilDestroyed, async pipe | `takeUntilDestroyed()`, `DestroyRef`, cuándo el async pipe es preferible |
| [docs/chapter18/part3.md](docs/chapter18/part3.md) | Operadores de acumulación: scan, reduce, buffer, window | `scan` para carrito reactivo, `reduce`, `bufferTime`, `bufferCount` |
| [docs/chapter18/part4.md](docs/chapter18/part4.md) | Testing de Observables con marble testing | `TestScheduler`, sintaxis de marble strings, `hot()`/`cold()`, tiempo virtual |

---

### PARTE X - Angular Signals: Reactividad Moderna
*Capítulos 19–20 · 8 archivos*

La trinidad reactiva de Signals, inputs y outputs modernos, interoperabilidad con RxJS, gestión de estado local, `resource()`, `httpResource()` y el camino a Zoneless.

| Archivo | Título | Descripción breve |
|---|---|---|
| [docs/chapter19/part1.md](docs/chapter19/part1.md) | ¿Qué son los Signals y cómo cambian Angular? | El problema con Zone.js, la trinidad signal→computed→effect, diagrama del grafo reactivo |
| [docs/chapter19/part2.md](docs/chapter19/part2.md) | signal(), computed() y effect(): la trinidad reactiva | `.set()`, `.update()`, `.mutate()`, `computed()` lazy, `effect()` con limpieza |
| [docs/chapter19/part3.md](docs/chapter19/part3.md) | Signal Inputs, Model Signals y output() | `input<T>()`, `input.required()`, `model<T>()` para two-way moderno, `output<T>()` |
| [docs/chapter19/part4.md](docs/chapter19/part4.md) | toSignal() y toObservable(): puente entre Signals y RxJS | `toSignal(obs$, { initialValue })`, `requireSync`, `toObservable(signal)`, errores comunes |
| [docs/chapter20/part1.md](docs/chapter20/part1.md) | Gestión de estado local con Signals en componentes | Reemplazar `BehaviorSubject` con `signal`, local store con `computed` y `effect` |
| [docs/chapter20/part2.md](docs/chapter20/part2.md) | Signals en formularios reactivos e HTTP | `linkedSignal`, `resource()`, `httpResource()`, estados `isLoading/error/value` |
| [docs/chapter20/part3.md](docs/chapter20/part3.md) | Signals y Change Detection: el camino a Zoneless Angular | Cómo Signals elimina Zone.js, `provideExperimentalZonelessChangeDetection()`, checklist |
| [docs/chapter20/part4.md](docs/chapter20/part4.md) | Signals vs RxJS: cuándo usar cada paradigma | Tabla de decisión, reglas prácticas, antipatrones, arquitectura de coexistencia |

---

### PARTE XI - Gestión de Estado con NgRx
*Capítulos 21–24 · 16 archivos*

NgRx completo: el patrón Redux, acciones, reducers, selectors memoizados, effects con RxJS, Entity, Router Store, DevTools y el moderno Signal Store.

| Archivo | Título | Descripción breve |
|---|---|---|
| [docs/chapter21/part1.md](docs/chapter21/part1.md) | El problema del estado y el patrón Redux | Prop drilling, servicios compartidos limitados, flujo unidireccional Redux |
| [docs/chapter21/part2.md](docs/chapter21/part2.md) | Instalación, configuración y arquitectura NgRx | `provideStore()`, estructura de carpetas por feature, paquetes del ecosistema |
| [docs/chapter21/part3.md](docs/chapter21/part3.md) | Actions: definiendo los eventos de la aplicación | `createAction`, `createActionGroup`, `props<T>()`, convención `[Fuente] Evento` |
| [docs/chapter21/part4.md](docs/chapter21/part4.md) | Reducers: transformando el estado de forma pura | `createReducer`, `on()`, inmutabilidad, `createFeature` con selectores automáticos |
| [docs/chapter22/part1.md](docs/chapter22/part1.md) | Selectors: consultando el estado de forma eficiente | `createFeatureSelector`, `createSelector`, composición, memoización automática |
| [docs/chapter22/part2.md](docs/chapter22/part2.md) | Selectors compuestos, memoización y createSelector | Selectors multi-feature, `defaultMemoize`, factory functions con parámetros |
| [docs/chapter22/part3.md](docs/chapter22/part3.md) | Effects: manejando efectos secundarios asincrónicos | `createEffect`, `ofType`, patrón action→HTTP→action, `dispatch: false` |
| [docs/chapter22/part4.md](docs/chapter22/part4.md) | Effects con operadores RxJS: switchMap, concatMap, error handling | Cuándo usar cada operador, `catchError` dentro del switchMap, tabla de decisión |
| [docs/chapter23/part1.md](docs/chapter23/part1.md) | NgRx Entity: colecciones normalizadas con EntityAdapter | `EntityState<T>`, `createEntityAdapter`, operaciones CRUD, selectores del adapter |
| [docs/chapter23/part2.md](docs/chapter23/part2.md) | NgRx Router Store: sincronizando router y store | `provideRouterStore()`, `selectUrl`, `selectRouteParams`, effects con navegación |
| [docs/chapter23/part3.md](docs/chapter23/part3.md) | NgRx DevTools: debugging con time-travel | Redux DevTools Extension, inspección de acciones, time-travel, `actionSanitizer` |
| [docs/chapter23/part4.md](docs/chapter23/part4.md) | Testing de NgRx: Actions, Reducers, Effects y Selectors | Testing de reducers puros, `MockStore`, `overrideSelector`, `provideMockActions` |
| [docs/chapter24/part1.md](docs/chapter24/part1.md) | Introducción al Signal Store: el nuevo paradigma NgRx | Motivación, primer `signalStore()`, comparación con store clásico |
| [docs/chapter24/part2.md](docs/chapter24/part2.md) | withState, withComputed y withMethods | `withState<T>()` genera Signals, `withComputed()`, `withMethods()`, `patchState()` |
| [docs/chapter24/part3.md](docs/chapter24/part3.md) | withHooks y store features personalizadas reutilizables | `onInit/onDestroy`, `withRequestStatus()`, `signalStoreFeature()`, composición |
| [docs/chapter24/part4.md](docs/chapter24/part4.md) | Migrando del NgRx Store clásico al Signal Store | Tabla de equivalencias, estrategia incremental, cuándo mantener el store clásico |

---

### PARTE XII - Optimización y Rendimiento
*Capítulos 25–27 · 12 archivos*

Change Detection en profundidad, OnPush, Zoneless, Virtual Scrolling, imágenes optimizadas, análisis de bundle, Core Web Vitals y SSR completo.

| Archivo | Título | Descripción breve |
|---|---|---|
| [docs/chapter25/part1.md](docs/chapter25/part1.md) | Cómo funciona Zone.js y el ciclo de Change Detection | Monkey-patching de APIs, cuándo se dispara el CD, árbol de componentes |
| [docs/chapter25/part2.md](docs/chapter25/part2.md) | Estrategia OnPush: cuándo y cómo usarla | Los 4 triggers de OnPush, inmutabilidad, antipatrones que lo rompen silenciosamente |
| [docs/chapter25/part3.md](docs/chapter25/part3.md) | ChangeDetectorRef: markForCheck, detach y control manual | `markForCheck()`, `detectChanges()`, `detach()`/`reattach()`, cuándo usarlos |
| [docs/chapter25/part4.md](docs/chapter25/part4.md) | Zoneless Angular con provideExperimentalZonelessChangeDetection | Eliminar Zone.js, qué deja de funcionar, checklist de migración |
| [docs/chapter26/part1.md](docs/chapter26/part1.md) | Virtual Scrolling con CDK: listas de miles de elementos | `cdk-virtual-scroll-viewport`, `*cdkVirtualFor`, `itemSize`, limitaciones |
| [docs/chapter26/part2.md](docs/chapter26/part2.md) | NgOptimizedImage: imágenes optimizadas out-of-the-box | `ngSrc`, `priority`, `fill`, `sizes`, loaders (Imgix, Cloudinary), impacto en LCP |
| [docs/chapter26/part3.md](docs/chapter26/part3.md) | Bundle analysis con webpack-bundle-analyzer y esbuild | `--stats-json`, treemap de dependencias, `source-map-explorer`, reducir bundle |
| [docs/chapter26/part4.md](docs/chapter26/part4.md) | Core Web Vitals en apps Angular: LCP, CLS y INP | Métricas de Google, causas específicas en Angular, checklist de 10 puntos |
| [docs/chapter27/part1.md](docs/chapter27/part1.md) | SSR con @angular/ssr: introducción e instalación | CSR vs SSR, `ng add @angular/ssr`, archivos generados, cuándo usar SSR |
| [docs/chapter27/part2.md](docs/chapter27/part2.md) | Hydration e TransferState: del servidor al cliente | `provideClientHydration()`, `TransferState`, `makeStateKey`, `withHttpTransferCache` |
| [docs/chapter27/part3.md](docs/chapter27/part3.md) | Static Site Generation (SSG) con prerender | SSG vs SSR, `"prerender": true`, rutas dinámicas, `PrerenderFallback` |
| [docs/chapter27/part4.md](docs/chapter27/part4.md) | SSR con autenticación, cookies y APIs privadas | Token `REQUEST`, cookies HttpOnly, `isPlatformBrowser`/`isPlatformServer`, `DOCUMENT` |

---

### PARTE XIII - Librerías Esenciales del Ecosistema
*Capítulos 28–31 · 16 archivos*

Angular Material (Material 3), CDK, Tailwind CSS y una suite completa de testing con Jest, Angular Testing Library y Playwright.

| Archivo | Título | Descripción breve |
|---|---|---|
| [docs/chapter28/part1.md](docs/chapter28/part1.md) | Instalación y theming con Design Tokens (Material 3) | `ng add @angular/material`, `mat-theme()`, paleta de colores, typography |
| [docs/chapter28/part2.md](docs/chapter28/part2.md) | Componentes de navegación: toolbar, sidenav, tabs, menu | `MatSidenav` responsivo con `BreakpointObserver`, `MatTabs`, `MatMenu` con submenús |
| [docs/chapter28/part3.md](docs/chapter28/part3.md) | Formularios y tablas: MatInput, MatSelect, MatTable, MatPaginator | `MatFormField`, `MatAutocomplete`, `MatTableDataSource` con sort y paginación |
| [docs/chapter28/part4.md](docs/chapter28/part4.md) | Overlays: MatDialog, MatSnackBar, MatBottomSheet | `MatDialog.open()`, `MAT_DIALOG_DATA`, `afterClosed()`, `MatSnackBar`, `MatBottomSheet` |
| [docs/chapter29/part1.md](docs/chapter29/part1.md) | Overlay y Portal: capas dinámicas de UI | `Overlay`, `ConnectedPositionStrategy`, `TemplatePortal`, `ComponentPortal`, ciclo de vida |
| [docs/chapter29/part2.md](docs/chapter29/part2.md) | Drag and Drop con DragDropModule | `cdkDrag`, `cdkDropList`, `moveItemInArray`, `transferArrayItem`, kanban con tres columnas |
| [docs/chapter29/part3.md](docs/chapter29/part3.md) | Accesibilidad con el paquete a11y del CDK | `FocusTrap`, `LiveAnnouncer`, `FocusMonitor`, `AriaDescriber`, dialog accesible |
| [docs/chapter29/part4.md](docs/chapter29/part4.md) | Stepper, Table y Virtual Scroll del CDK | `CdkStepper` sin estilos Material, `CdkTableModule`, stepper de onboarding personalizado |
| [docs/chapter30/part1.md](docs/chapter30/part1.md) | Instalación y configuración de Tailwind en Angular | `tailwind.config.js` con `content` para templates Angular, integración con esbuild, purging |
| [docs/chapter30/part2.md](docs/chapter30/part2.md) | Construyendo componentes UI con clases utilitarias | Utility-first en templates, `@apply` en SCSS, componentes Card/Alert/Badge con Tailwind |
| [docs/chapter30/part3.md](docs/chapter30/part3.md) | Responsive design y Dark Mode con Tailwind | Breakpoints `sm:/md:/lg:`, `darkMode: 'class'`, toggle con Signal, `prefers-color-scheme` |
| [docs/chapter30/part4.md](docs/chapter30/part4.md) | Tailwind + Angular Material: convivencia armoniosa | Desactivar preflight, `@layer`, estrategia híbrida Material+Tailwind para proyectos reales |
| [docs/chapter31/part1.md](docs/chapter31/part1.md) | Testing unitario con Jest: setup y primeras pruebas | Migrar de Karma a Jest, `jest-preset-angular`, `TestBed`, primer test de componente standalone |
| [docs/chapter31/part2.md](docs/chapter31/part2.md) | Testing de componentes con Angular Testing Library | `render()`, `screen.getByRole()`, `userEvent`, filosofía de testing por comportamiento |
| [docs/chapter31/part3.md](docs/chapter31/part3.md) | Testing de servicios, HTTP y NgRx | `HttpTestingController`, `MockStore`, `overrideSelector`, testing de effects |
| [docs/chapter31/part4.md](docs/chapter31/part4.md) | E2E Testing con Playwright en proyectos Angular | `playwright.config.ts`, queries accesibles, Page Object Model, CI con GitHub Actions |

---

### PARTE XIV - Arquitectura y Patrones Avanzados
*Capítulos 32–35 · 16 archivos*

Patrones de arquitectura escalable, micro-frontends con Module Federation y Native Federation, internacionalización, accesibilidad avanzada y despliegue en producción.

| Archivo | Título | Descripción breve |
|---|---|---|
| [docs/chapter32/part1.md](docs/chapter32/part1.md) | Arquitectura por features y dominios escalables | Feature-based structure, barrel exports con `index.ts`, separación UI/dominio |
| [docs/chapter32/part2.md](docs/chapter32/part2.md) | Smart Components y Dumb Components | Container vs Presentational, reglas para cada tipo, relación con OnPush y testing |
| [docs/chapter32/part3.md](docs/chapter32/part3.md) | Facade Pattern con servicios y NgRx | `ProductosFacade` que abstrae el store, ventajas en testing, cuándo es overhead |
| [docs/chapter32/part4.md](docs/chapter32/part4.md) | Nx Workspace: monorepos y arquitectura de librerías | `create-nx-workspace`, tagging de librerías, `nx affected:test`, `enforce-module-boundaries` |
| [docs/chapter33/part1.md](docs/chapter33/part1.md) | ¿Qué son los micro-frontends y cuándo usarlos? | Motivación, patrones de composición (client-side/server-side), cuándo NO usar MFE |
| [docs/chapter33/part2.md](docs/chapter33/part2.md) | Webpack Module Federation con Angular | Host y remote con `@angular-architects/module-federation`, `shared`, versioning |
| [docs/chapter33/part3.md](docs/chapter33/part3.md) | Native Federation: Module Federation sin Webpack | Import Maps nativos, `federation.config.js`, `initFederation()` en `main.ts`, comparativa |
| [docs/chapter33/part4.md](docs/chapter33/part4.md) | Comunicación entre micro-frontends: eventos y estado compartido | Custom Events, `BroadcastChannel`, shell como mediador de autenticación, qué NO compartir |
| [docs/chapter34/part1.md](docs/chapter34/part1.md) | i18n nativo con @angular/localize | Atributo `i18n`, `ng extract-i18n`, XLIFF, `ng build --localize`, un build por locale |
| [docs/chapter34/part2.md](docs/chapter34/part2.md) | Transloco: la alternativa moderna para i18n en runtime | `@jsverse/transloco`, JSON de traducciones, cambio de idioma sin recargar, lazy loading |
| [docs/chapter34/part3.md](docs/chapter34/part3.md) | Accesibilidad (a11y): semántica, roles ARIA y Angular | HTML semántico, `aria-label`, `aria-live`, gestión del foco en SPAs |
| [docs/chapter34/part4.md](docs/chapter34/part4.md) | Patrones ARIA avanzados y auditoría de accesibilidad | Dialog/Combobox/Tabs accesibles, `axe-core` en tests, Lighthouse en CI |
| [docs/chapter35/part1.md](docs/chapter35/part1.md) | Configuración de entornos: environment.ts y variables de entorno | `fileReplacements`, `APP_CONFIG` con `InjectionToken`, config en runtime con `APP_INITIALIZER` |
| [docs/chapter35/part2.md](docs/chapter35/part2.md) | CI/CD con GitHub Actions: build, test y deploy automático | Workflow YAML completo, caché de `node_modules`, deploy a GitHub Pages/Firebase/Vercel |
| [docs/chapter35/part3.md](docs/chapter35/part3.md) | Dockerización de apps Angular y deploy en cloud | Dockerfile multi-stage, `nginx.conf` para SPA, Cloud Run y ECS Fargate |
| [docs/chapter35/part4.md](docs/chapter35/part4.md) | Monitoreo, error tracking con Sentry y analytics | `@sentry/angular`, `ErrorHandler`, GA4 con consent management, GDPR |

---

### PARTE XV - Angular 20 y el Futuro del Framework
*Capítulo 36 · 4 archivos*

Las novedades estables de Angular 20: `@let` en templates, signal-based queries, `linkedSignal()` y `resource()` estables, hydratación incremental, modos de renderizado por ruta, HMR mejorado, y el roadmap hacia Angular 21 con Zoneless estable y Signal Forms.

| Archivo | Título | Descripción breve |
|---|---|---|
| [docs/chapter36/part1.md](docs/chapter36/part1.md) | `@let` en templates y signal-based queries | Declaración de variables locales reactivas, `viewChild()`/`contentChild()` como Signals |
| [docs/chapter36/part2.md](docs/chapter36/part2.md) | linkedSignal(), resource() y httpResource() en Angular 20 | APIs promovidas a developer preview/estable, comparativa con enfoques anteriores |
| [docs/chapter36/part3.md](docs/chapter36/part3.md) | Hydratación incremental y modos de renderizado por ruta | `withIncrementalHydration()`, `@defer hydrate on`, `RenderMode` por ruta en `app.routes.server.ts` |
| [docs/chapter36/part4.md](docs/chapter36/part4.md) | Zoneless, Angular 21 y el roadmap del framework | `provideZonelessChangeDetection()` estable, Signal Forms, `@angular/build`, hoja de ruta |

---

## Resumen de la guía

| Métrica | Valor |
|---|---|
| Partes | 15 |
| Capítulos | 36 |
| Archivos de contenido | 144 |
| Versiones cubiertas | Angular 15 → 21 |
| Idioma | Español neutro latinoamericano |
| Estilo de código | TypeScript strict, Angular 17+ standalone |
| Diagramas | Mermaid (sin ASCII art) |

---

*Esta guía es un documento vivo. Las secciones de Angular 20 y 21 reflejan las APIs estables y developer preview documentadas en los changelogs oficiales.*

---

## Contribuidores

Esta guía fue redactada en colaboración con [Claude Code](https://claude.ai/code) (Anthropic), que participó activamente en la escritura de capítulos, la revisión de ejemplos de código, la coherencia terminológica y la estructuración del contenido a lo largo de los 36 capítulos.

Gracias a todas las personas que contribuyan con correcciones, sugerencias y mejoras a través de issues y pull requests.
