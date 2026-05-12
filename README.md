# Angular: De Cero a Experto — La Guía Definitiva en Español

> La guía más completa de Angular en español. Cubre Angular 17–21 desde los fundamentos hasta arquitecturas de nivel enterprise, con Signals, NgRx, SSR, micro-frontends y todo lo nuevo en Angular 20 y 21.

---

## ¿Qué es esta guía?

Esta guía está escrita para desarrolladores hispanohablantes que quieren dominar Angular de verdad — no solo aprender la sintaxis, sino entender el *por qué* detrás de cada decisión de diseño del framework. Cada concepto se explica como lo haría un senior a un colega: directo, honesto y con ejemplos que resuelven problemas reales.

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

### PARTE I — Primeros Pasos con Angular
*Capítulos 1–2 · 8 archivos*

Cubre la historia del framework, el ecosistema de herramientas, la estructura de un proyecto y el proceso de arranque. Ideal para quien nunca ha tocado Angular.

| Archivo | Título | Descripción breve |
|---|---|---|
| [capitulo01-parte1.md](capitulo01-parte1.md) | Historia, versiones y el renacimiento de Angular | De AngularJS a Angular 2+, el ciclo de releases semver, la era Ivy y Standalone |
| [capitulo01-parte2.md](capitulo01-parte2.md) | Angular vs React vs Vue: cuándo elegir cada uno | Comparativa sin favoritismos; casos donde Angular brilla (enterprise, tipado estricto) |
| [capitulo01-parte3.md](capitulo01-parte3.md) | Instalación de Node, Angular CLI y VS Code | Setup completo del entorno con extensiones recomendadas y diagrama del toolchain |
| [capitulo01-parte4.md](capitulo01-parte4.md) | Tu primera aplicación: ng new al primer ng serve | Crear un proyecto, explorar la estructura y hacer el primer cambio con live reload |
| [capitulo02-parte1.md](capitulo02-parte1.md) | Visión general: módulos, componentes, servicios | Diagrama de cómo se relacionan los bloques principales de Angular |
| [capitulo02-parte2.md](capitulo02-parte2.md) | Angular CLI a fondo: comandos esenciales y schematics | `ng generate`, `ng build`, `ng test`, `ng lint`, flags útiles como `--dry-run` |
| [capitulo02-parte3.md](capitulo02-parte3.md) | Estructura de carpetas y convenciones de proyecto | Feature-based structure, barrel exports, convenciones de nombres kebab-case/PascalCase |
| [capitulo02-parte4.md](capitulo02-parte4.md) | El proceso de arranque: main.ts, AppModule y bootstrap | `bootstrapApplication()`, `APP_INITIALIZER`, `provideRouter`, `provideHttpClient` |

---

### PARTE II — Componentes: El Alma de Angular
*Capítulos 3–4 · 8 archivos*

Todo lo que necesitas saber sobre componentes: desde la anatomía básica hasta técnicas avanzadas de proyección de contenido y carga diferida de UI.

| Archivo | Título | Descripción breve |
|---|---|---|
| [capitulo03-parte1.md](capitulo03-parte1.md) | Anatomía de un componente: clase, decorador y template | Las tres partes de un componente, el decorador `@Component` y sus propiedades |
| [capitulo03-parte2.md](capitulo03-parte2.md) | Ciclo de vida: OnInit, OnChanges, OnDestroy y los demás | Los 8 hooks en orden de ejecución con casos de uso y diagrama Mermaid |
| [capitulo03-parte3.md](capitulo03-parte3.md) | Comunicación con @Input y @Output | `@Input()` con alias y transformaciones, `@Output()` con `EventEmitter`, patrón padre-hijo |
| [capitulo03-parte4.md](capitulo03-parte4.md) | Estilos en componentes: encapsulación y ViewEncapsulation | `Emulated`, `None`, `ShadowDom`, `:host`, variables CSS, theming |
| [capitulo04-parte1.md](capitulo04-parte1.md) | ViewChild, ViewChildren y ElementRef | `@ViewChild` con tipos de referencia, `QueryList`, `static: true` vs `false` |
| [capitulo04-parte2.md](capitulo04-parte2.md) | ng-content: proyección de contenido simple y múltiple | `<ng-content>`, proyección con `select`, `ContentChild`, componente card reutilizable |
| [capitulo04-parte3.md](capitulo04-parte3.md) | Componentes Standalone: el futuro de Angular | `standalone: true`, `imports` en el decorador, bootstrap sin NgModule |
| [capitulo04-parte4.md](capitulo04-parte4.md) | Deferrable Views con @defer: carga diferida de UI | `@defer`, `@loading`, `@error`, triggers de viewport/interacción/timer, impacto en LCP |

---

### PARTE III — Templates y Directivas
*Capítulos 5–6 · 8 archivos*

Data binding en todas sus formas, la nueva sintaxis de control de flujo y cómo crear directivas personalizadas de atributo y estructurales.

| Archivo | Título | Descripción breve |
|---|---|---|
| [capitulo05-parte1.md](capitulo05-parte1.md) | Interpolación y Property Binding | `{{ }}`, `[prop]`, attribute vs property binding, `[class.x]`, `[style.y]` |
| [capitulo05-parte2.md](capitulo05-parte2.md) | Event Binding y Two-way Binding | `(evento)`, `$event`, `[(ngModel)]`, two-way con Signal inputs |
| [capitulo05-parte3.md](capitulo05-parte3.md) | Template Reference Variables y @ViewChild | `#refVar` en templates, pasar refs a métodos, diferencias entre enfoques |
| [capitulo05-parte4.md](capitulo05-parte4.md) | Nueva sintaxis de control de flujo: @if, @for, @switch | `@if/@else if/@else`, `@for` con `track` obligatorio, `@switch`, diferencias con `*ngIf` legacy |
| [capitulo06-parte1.md](capitulo06-parte1.md) | Directivas estructurales built-in: ngIf, ngFor, ngSwitch | `*ngIf`, `ngIfThen`, `*ngFor` con `index/first/last`, cuándo migrar a nueva sintaxis |
| [capitulo06-parte2.md](capitulo06-parte2.md) | Directivas de atributo built-in: ngClass, ngStyle | `[ngClass]` con objeto/array/string, `[ngStyle]`, diferencias con bindings directos |
| [capitulo06-parte3.md](capitulo06-parte3.md) | Creando directivas de atributo personalizadas | `@Directive`, `Renderer2`, directiva `appResaltado` con `@HostListener` |
| [capitulo06-parte4.md](capitulo06-parte4.md) | HostListener, HostBinding y directivas estructurales propias | `@HostListener`, `@HostBinding`, directiva estructural con `TemplateRef` y `ViewContainerRef` |

---

### PARTE IV — Pipes: Transformando Datos
*Capítulo 7 · 4 archivos*

Los pipes built-in de Angular, cómo encadenarlos y parametrizarlos, y cómo crear pipes personalizados con control total del rendimiento.

| Archivo | Título | Descripción breve |
|---|---|---|
| [capitulo07-parte1.md](capitulo07-parte1.md) | Pipes built-in: date, currency, number, json, async | `DatePipe`, `CurrencyPipe`, `DecimalPipe`, `AsyncPipe` con Observable y Promise, `LOCALE_ID` |
| [capitulo07-parte2.md](capitulo07-parte2.md) | Parámetros de pipes y encadenamiento | Sintaxis `\| pipe:param1:param2`, encadenamiento múltiple, orden de evaluación |
| [capitulo07-parte3.md](capitulo07-parte3.md) | Creando pipes personalizados con PipeTransform | `@Pipe({ name, standalone, pure })`, ejemplo `filtrarPor` y `truncarTexto` |
| [capitulo07-parte4.md](capitulo07-parte4.md) | Pipes puros vs impuros: impacto en rendimiento | Qué es un pipe puro, cuándo necesitas `pure: false` y el costo, alternativas |

---

### PARTE V — Servicios e Inyección de Dependencias
*Capítulos 8–9 · 8 archivos*

La arquitectura de capas de Angular, el sistema de DI, la jerarquía de inyectores y la migración completa del mundo NgModules al mundo Standalone.

| Archivo | Título | Descripción breve |
|---|---|---|
| [capitulo08-parte1.md](capitulo08-parte1.md) | ¿Qué es un servicio? Responsabilidad única y separación de capas | Problema que resuelven, diagrama de capas (presentación / lógica / datos) |
| [capitulo08-parte2.md](capitulo08-parte2.md) | Creando e inyectando servicios | `@Injectable({ providedIn: 'root' })`, inyección por constructor vs `inject()` |
| [capitulo08-parte3.md](capitulo08-parte3.md) | Inyección de Dependencias: el sistema DI de Angular | Tokens de inyección, `InjectionToken<T>`, `@Inject()`, `inject()` en funciones puras |
| [capitulo08-parte4.md](capitulo08-parte4.md) | Jerarquía de inyectores: root, módulo y componente | Árbol de inyectores, resolución de dependencias, instancias separadas por componente |
| [capitulo09-parte1.md](capitulo09-parte1.md) | NgModules: declarations, imports, exports, providers | Anatomía de `@NgModule`, qué va en cada array, errores comunes |
| [capitulo09-parte2.md](capitulo09-parte2.md) | Módulo Core, Shared y de funcionalidad | Patrón de tres tipos de módulos, `forRoot()` para evitar importar CoreModule dos veces |
| [capitulo09-parte3.md](capitulo09-parte3.md) | El mundo Standalone: componentes, directivas y pipes sin módulo | `standalone: true`, imports en el decorador, ventajas en tree-shaking, `importProvidersFrom` |
| [capitulo09-parte4.md](capitulo09-parte4.md) | Guía de migración: de NgModules a Standalone | Comando automático `ng generate @angular/core:standalone`, fases, compatibilidad híbrida |

---

### PARTE VI — Navegación y Routing
*Capítulos 10–11 · 8 archivos*

Configuración del router, navegación programática, rutas dinámicas, lazy loading, guards funcionales y estrategias de preloading.

| Archivo | Título | Descripción breve |
|---|---|---|
| [capitulo10-parte1.md](capitulo10-parte1.md) | Configuración del Router: provideRouter y rutas básicas | `provideRouter(routes)`, objeto de ruta, `redirectTo`, `pathMatch`, ruta wildcard `**` |
| [capitulo10-parte2.md](capitulo10-parte2.md) | RouterLink, RouterOutlet y navegación programática | `<router-outlet>`, `[routerLink]`, `routerLinkActive`, `Router.navigate()` |
| [capitulo10-parte3.md](capitulo10-parte3.md) | Rutas con parámetros :id y Query Params | `paramMap` como Observable, `queryParams`, `fragment`, lectura con `inject(ActivatedRoute)` |
| [capitulo10-parte4.md](capitulo10-parte4.md) | Rutas hijas (Child Routes) y outlets secundarios | `children` en rutas, `<router-outlet>` anidado, outlets con nombre |
| [capitulo11-parte1.md](capitulo11-parte1.md) | Lazy Loading: cargando módulos y componentes bajo demanda | `loadComponent`, `loadChildren`, impacto en bundle size, verificar chunks en DevTools |
| [capitulo11-parte2.md](capitulo11-parte2.md) | Guards funcionales: canActivate, canDeactivate, canMatch | Guards como funciones (Angular 14+), `inject()` dentro del guard, redirigir desde guard |
| [capitulo11-parte3.md](capitulo11-parte3.md) | Resolvers: precargando datos antes de navegar | `ResolveFn<T>`, acceder a datos resueltos, cuándo NO usar resolvers, alternativa con Signals |
| [capitulo11-parte4.md](capitulo11-parte4.md) | Estrategias de preloading: PreloadAllModules y personalizadas | `PreloadAllModules`, estrategia personalizada, preloading selectivo, `QuicklinkStrategy` |

---

### PARTE VII — Formularios
*Capítulos 12–13 · 8 archivos*

Los dos enfoques de formularios en Angular: template-driven para casos simples y reactive forms para validación compleja, dinámismo y control total.

| Archivo | Título | Descripción breve |
|---|---|---|
| [capitulo12-parte1.md](capitulo12-parte1.md) | Fundamentos: ngModel, ngForm y FormsModule | `[(ngModel)]`, `ngForm`, `form.valid`, `form.value`, submit con `(ngSubmit)` |
| [capitulo12-parte2.md](capitulo12-parte2.md) | Validación con atributos HTML y directivas de Angular | `required`, `minlength`, `pattern`, clases CSS `ng-valid/ng-invalid/ng-touched` |
| [capitulo12-parte3.md](capitulo12-parte3.md) | Mensajes de error y clases CSS de estado | Estrategias para mostrar errores, componente de campo reutilizable, reset de formulario |
| [capitulo12-parte4.md](capitulo12-parte4.md) | Formularios anidados con ngModelGroup | `ngModelGroup` para agrupar campos, acceder a subgrupos, validación de grupo |
| [capitulo13-parte1.md](capitulo13-parte1.md) | FormControl, FormGroup y FormBuilder | `new FormControl<T>()`, `FormBuilder.group()`, `FormBuilder.nonNullable`, tipado genérico |
| [capitulo13-parte2.md](capitulo13-parte2.md) | Validators síncronos y asíncronos built-in | `Validators.required/email/min/max/pattern`, `AsyncValidatorFn` con `debounceTime` |
| [capitulo13-parte3.md](capitulo13-parte3.md) | FormArray: listas dinámicas de controles | `FormArray`, `push()`, `removeAt()`, tipado genérico, validación del array completo |
| [capitulo13-parte4.md](capitulo13-parte4.md) | Validadores personalizados y cross-field validation | `ValidatorFn`, validación de contraseñas iguales, `AsyncValidatorFn` que consulta una API |

---

### PARTE VIII — Comunicación HTTP
*Capítulos 14–15 · 8 archivos*

`HttpClient` con tipado genérico, manejo de errores, interceptores funcionales para autenticación, loading global y caché con RxJS.

| Archivo | Título | Descripción breve |
|---|---|---|
| [capitulo14-parte1.md](capitulo14-parte1.md) | Configuración con provideHttpClient y primera petición GET | `provideHttpClient()`, inyectar `HttpClient`, primer `get<T>()`, async pipe |
| [capitulo14-parte2.md](capitulo14-parte2.md) | POST, PUT, PATCH, DELETE con tipado genérico | Métodos HTTP con body tipado, interfaces de respuesta, opciones por request |
| [capitulo14-parte3.md](capitulo14-parte3.md) | Manejo de errores con catchError y tipado de respuestas | `HttpErrorResponse`, `catchError`, errores de cliente vs servidor, estrategias de notificación |
| [capitulo14-parte4.md](capitulo14-parte4.md) | Headers, params, HttpContext y opciones avanzadas | `HttpHeaders`, `HttpParams`, `observe: 'response'`, `reportProgress`, `HttpContext` |
| [capitulo15-parte1.md](capitulo15-parte1.md) | Interceptores funcionales (Angular 15+): concepto y estructura | `HttpInterceptorFn`, `request.clone()`, `withInterceptors([])`, orden de ejecución |
| [capitulo15-parte2.md](capitulo15-parte2.md) | Interceptor de autenticación: adjuntando JWT automáticamente | Leer token desde servicio, `Authorization: Bearer`, excluir URLs públicas, manejar 401 |
| [capitulo15-parte3.md](capitulo15-parte3.md) | Interceptor de loading global y manejo centralizado de errores | Contador con Signal, spinner global, interceptor de errores con toast, `finalize()` |
| [capitulo15-parte4.md](capitulo15-parte4.md) | Estrategias de caché HTTP y retry con RxJS | `shareReplay(1)`, caché con `Map`, `retry(3)`, backoff exponencial con `retryWhen` |

---

### PARTE IX — Programación Reactiva con RxJS
*Capítulos 16–18 · 12 archivos*

RxJS de cero a avanzado: Observables, Subjects, operadores de transformación/filtrado/combinación, patrones reactivos en servicios y marble testing.

| Archivo | Título | Descripción breve |
|---|---|---|
| [capitulo16-parte1.md](capitulo16-parte1.md) | ¿Qué es la programación reactiva? Observables vs Promesas | Push vs pull, lazy vs eager, unicast vs multicast, diagrama comparativo |
| [capitulo16-parte2.md](capitulo16-parte2.md) | Observable, Observer, Subscription y el contrato reactivo | Anatomía del Observable, `next/error/complete`, cold vs hot, `unsubscribe()` |
| [capitulo16-parte3.md](capitulo16-parte3.md) | Subject, BehaviorSubject, ReplaySubject y AsyncSubject | Cuándo usar cada tipo de Subject, comparativa con diagrama Mermaid |
| [capitulo16-parte4.md](capitulo16-parte4.md) | Creadores: of, from, interval, timer, fromEvent | `of`, `from`, `interval`, `timer`, `fromEvent`, `EMPTY`, `NEVER`, `throwError` |
| [capitulo17-parte1.md](capitulo17-parte1.md) | Transformación: map, switchMap, mergeMap, concatMap, exhaustMap | Diferencias críticas entre los cuatro operadores de aplanamiento con ejemplos reales |
| [capitulo17-parte2.md](capitulo17-parte2.md) | Filtrado: filter, take, first, debounceTime, distinctUntilChanged | Buscador con `debounceTime(300)` + `distinctUntilChanged` + `switchMap` |
| [capitulo17-parte3.md](capitulo17-parte3.md) | Combinación: combineLatest, forkJoin, zip, withLatestFrom | Peticiones paralelas, combinar filtros reactivos, sincronización de streams |
| [capitulo17-parte4.md](capitulo17-parte4.md) | Manejo de errores: catchError, retry, retryWhen, throwError | `catchError` con alternativa o re-lanzamiento, backoff exponencial, `finalize` |
| [capitulo18-parte1.md](capitulo18-parte1.md) | Patrones reactivos en servicios Angular | State service con `BehaviorSubject`, `asObservable()`, `shareReplay(1)` |
| [capitulo18-parte2.md](capitulo18-parte2.md) | Evitando memory leaks: takeUntilDestroyed, async pipe | `takeUntilDestroyed()`, `DestroyRef`, cuándo el async pipe es preferible |
| [capitulo18-parte3.md](capitulo18-parte3.md) | Operadores de acumulación: scan, reduce, buffer, window | `scan` para carrito reactivo, `reduce`, `bufferTime`, `bufferCount` |
| [capitulo18-parte4.md](capitulo18-parte4.md) | Testing de Observables con marble testing | `TestScheduler`, sintaxis de marble strings, `hot()`/`cold()`, tiempo virtual |

---

### PARTE X — Angular Signals: Reactividad Moderna
*Capítulos 19–20 · 8 archivos*

La trinidad reactiva de Signals, inputs y outputs modernos, interoperabilidad con RxJS, gestión de estado local, `resource()`, `httpResource()` y el camino a Zoneless.

| Archivo | Título | Descripción breve |
|---|---|---|
| [capitulo19-parte1.md](capitulo19-parte1.md) | ¿Qué son los Signals y cómo cambian Angular? | El problema con Zone.js, la trinidad signal→computed→effect, diagrama del grafo reactivo |
| [capitulo19-parte2.md](capitulo19-parte2.md) | signal(), computed() y effect(): la trinidad reactiva | `.set()`, `.update()`, `.mutate()`, `computed()` lazy, `effect()` con limpieza |
| [capitulo19-parte3.md](capitulo19-parte3.md) | Signal Inputs, Model Signals y output() | `input<T>()`, `input.required()`, `model<T>()` para two-way moderno, `output<T>()` |
| [capitulo19-parte4.md](capitulo19-parte4.md) | toSignal() y toObservable(): puente entre Signals y RxJS | `toSignal(obs$, { initialValue })`, `requireSync`, `toObservable(signal)`, errores comunes |
| [capitulo20-parte1.md](capitulo20-parte1.md) | Gestión de estado local con Signals en componentes | Reemplazar `BehaviorSubject` con `signal`, local store con `computed` y `effect` |
| [capitulo20-parte2.md](capitulo20-parte2.md) | Signals en formularios reactivos e HTTP | `linkedSignal`, `resource()`, `httpResource()`, estados `isLoading/error/value` |
| [capitulo20-parte3.md](capitulo20-parte3.md) | Signals y Change Detection: el camino a Zoneless Angular | Cómo Signals elimina Zone.js, `provideExperimentalZonelessChangeDetection()`, checklist |
| [capitulo20-parte4.md](capitulo20-parte4.md) | Signals vs RxJS: cuándo usar cada paradigma | Tabla de decisión, reglas prácticas, antipatrones, arquitectura de coexistencia |

---

### PARTE XI — Gestión de Estado con NgRx
*Capítulos 21–24 · 16 archivos*

NgRx completo: el patrón Redux, acciones, reducers, selectors memoizados, effects con RxJS, Entity, Router Store, DevTools y el moderno Signal Store.

| Archivo | Título | Descripción breve |
|---|---|---|
| [capitulo21-parte1.md](capitulo21-parte1.md) | El problema del estado y el patrón Redux | Prop drilling, servicios compartidos limitados, flujo unidireccional Redux |
| [capitulo21-parte2.md](capitulo21-parte2.md) | Instalación, configuración y arquitectura NgRx | `provideStore()`, estructura de carpetas por feature, paquetes del ecosistema |
| [capitulo21-parte3.md](capitulo21-parte3.md) | Actions: definiendo los eventos de la aplicación | `createAction`, `createActionGroup`, `props<T>()`, convención `[Fuente] Evento` |
| [capitulo21-parte4.md](capitulo21-parte4.md) | Reducers: transformando el estado de forma pura | `createReducer`, `on()`, inmutabilidad, `createFeature` con selectores automáticos |
| [capitulo22-parte1.md](capitulo22-parte1.md) | Selectors: consultando el estado de forma eficiente | `createFeatureSelector`, `createSelector`, composición, memoización automática |
| [capitulo22-parte2.md](capitulo22-parte2.md) | Selectors compuestos, memoización y createSelector | Selectors multi-feature, `defaultMemoize`, factory functions con parámetros |
| [capitulo22-parte3.md](capitulo22-parte3.md) | Effects: manejando efectos secundarios asincrónicos | `createEffect`, `ofType`, patrón action→HTTP→action, `dispatch: false` |
| [capitulo22-parte4.md](capitulo22-parte4.md) | Effects con operadores RxJS: switchMap, concatMap, error handling | Cuándo usar cada operador, `catchError` dentro del switchMap, tabla de decisión |
| [capitulo23-parte1.md](capitulo23-parte1.md) | NgRx Entity: colecciones normalizadas con EntityAdapter | `EntityState<T>`, `createEntityAdapter`, operaciones CRUD, selectores del adapter |
| [capitulo23-parte2.md](capitulo23-parte2.md) | NgRx Router Store: sincronizando router y store | `provideRouterStore()`, `selectUrl`, `selectRouteParams`, effects con navegación |
| [capitulo23-parte3.md](capitulo23-parte3.md) | NgRx DevTools: debugging con time-travel | Redux DevTools Extension, inspección de acciones, time-travel, `actionSanitizer` |
| [capitulo23-parte4.md](capitulo23-parte4.md) | Testing de NgRx: Actions, Reducers, Effects y Selectors | Testing de reducers puros, `MockStore`, `overrideSelector`, `provideMockActions` |
| [capitulo24-parte1.md](capitulo24-parte1.md) | Introducción al Signal Store: el nuevo paradigma NgRx | Motivación, primer `signalStore()`, comparación con store clásico |
| [capitulo24-parte2.md](capitulo24-parte2.md) | withState, withComputed y withMethods | `withState<T>()` genera Signals, `withComputed()`, `withMethods()`, `patchState()` |
| [capitulo24-parte3.md](capitulo24-parte3.md) | withHooks y store features personalizadas reutilizables | `onInit/onDestroy`, `withRequestStatus()`, `signalStoreFeature()`, composición |
| [capitulo24-parte4.md](capitulo24-parte4.md) | Migrando del NgRx Store clásico al Signal Store | Tabla de equivalencias, estrategia incremental, cuándo mantener el store clásico |

---

### PARTE XII — Optimización y Rendimiento
*Capítulos 25–27 · 12 archivos*

Change Detection en profundidad, OnPush, Zoneless, Virtual Scrolling, imágenes optimizadas, análisis de bundle, Core Web Vitals y SSR completo.

| Archivo | Título | Descripción breve |
|---|---|---|
| [capitulo25-parte1.md](capitulo25-parte1.md) | Cómo funciona Zone.js y el ciclo de Change Detection | Monkey-patching de APIs, cuándo se dispara el CD, árbol de componentes |
| [capitulo25-parte2.md](capitulo25-parte2.md) | Estrategia OnPush: cuándo y cómo usarla | Los 4 triggers de OnPush, inmutabilidad, antipatrones que lo rompen silenciosamente |
| [capitulo25-parte3.md](capitulo25-parte3.md) | ChangeDetectorRef: markForCheck, detach y control manual | `markForCheck()`, `detectChanges()`, `detach()`/`reattach()`, cuándo usarlos |
| [capitulo25-parte4.md](capitulo25-parte4.md) | Zoneless Angular con provideExperimentalZonelessChangeDetection | Eliminar Zone.js, qué deja de funcionar, checklist de migración |
| [capitulo26-parte1.md](capitulo26-parte1.md) | Virtual Scrolling con CDK: listas de miles de elementos | `cdk-virtual-scroll-viewport`, `*cdkVirtualFor`, `itemSize`, limitaciones |
| [capitulo26-parte2.md](capitulo26-parte2.md) | NgOptimizedImage: imágenes optimizadas out-of-the-box | `ngSrc`, `priority`, `fill`, `sizes`, loaders (Imgix, Cloudinary), impacto en LCP |
| [capitulo26-parte3.md](capitulo26-parte3.md) | Bundle analysis con webpack-bundle-analyzer y esbuild | `--stats-json`, treemap de dependencias, `source-map-explorer`, reducir bundle |
| [capitulo26-parte4.md](capitulo26-parte4.md) | Core Web Vitals en apps Angular: LCP, CLS y INP | Métricas de Google, causas específicas en Angular, checklist de 10 puntos |
| [capitulo27-parte1.md](capitulo27-parte1.md) | SSR con @angular/ssr: introducción e instalación | CSR vs SSR, `ng add @angular/ssr`, archivos generados, cuándo usar SSR |
| [capitulo27-parte2.md](capitulo27-parte2.md) | Hydration e TransferState: del servidor al cliente | `provideClientHydration()`, `TransferState`, `makeStateKey`, `withHttpTransferCache` |
| [capitulo27-parte3.md](capitulo27-parte3.md) | Static Site Generation (SSG) con prerender | SSG vs SSR, `"prerender": true`, rutas dinámicas, `PrerenderFallback` |
| [capitulo27-parte4.md](capitulo27-parte4.md) | SSR con autenticación, cookies y APIs privadas | Token `REQUEST`, cookies HttpOnly, `isPlatformBrowser`/`isPlatformServer`, `DOCUMENT` |

---

### PARTE XIII — Librerías Esenciales del Ecosistema
*Capítulos 28–31 · 16 archivos*

Angular Material (Material 3), CDK, Tailwind CSS y una suite completa de testing con Jest, Angular Testing Library y Playwright.

| Archivo | Título | Descripción breve |
|---|---|---|
| [capitulo28-parte1.md](capitulo28-parte1.md) | Instalación y theming con Design Tokens (Material 3) | `ng add @angular/material`, `mat-theme()`, paleta de colores, typography |
| [capitulo28-parte2.md](capitulo28-parte2.md) | Componentes de navegación: toolbar, sidenav, tabs, menu | `MatSidenav` responsivo con `BreakpointObserver`, `MatTabs`, `MatMenu` con submenús |
| [capitulo28-parte3.md](capitulo28-parte3.md) | Formularios y tablas: MatInput, MatSelect, MatTable, MatPaginator | `MatFormField`, `MatAutocomplete`, `MatTableDataSource` con sort y paginación |
| [capitulo28-parte4.md](capitulo28-parte4.md) | Overlays: MatDialog, MatSnackBar, MatBottomSheet | `MatDialog.open()`, `MAT_DIALOG_DATA`, `afterClosed()`, `MatSnackBar`, `MatBottomSheet` |
| [capitulo29-parte1.md](capitulo29-parte1.md) | Overlay y Portal: capas dinámicas de UI | `Overlay`, `ConnectedPositionStrategy`, `TemplatePortal`, `ComponentPortal`, ciclo de vida |
| [capitulo29-parte2.md](capitulo29-parte2.md) | Drag and Drop con DragDropModule | `cdkDrag`, `cdkDropList`, `moveItemInArray`, `transferArrayItem`, kanban con tres columnas |
| [capitulo29-parte3.md](capitulo29-parte3.md) | Accesibilidad con el paquete a11y del CDK | `FocusTrap`, `LiveAnnouncer`, `FocusMonitor`, `AriaDescriber`, dialog accesible |
| [capitulo29-parte4.md](capitulo29-parte4.md) | Stepper, Table y Virtual Scroll del CDK | `CdkStepper` sin estilos Material, `CdkTableModule`, stepper de onboarding personalizado |
| [capitulo30-parte1.md](capitulo30-parte1.md) | Instalación y configuración de Tailwind en Angular | `tailwind.config.js` con `content` para templates Angular, integración con esbuild, purging |
| [capitulo30-parte2.md](capitulo30-parte2.md) | Construyendo componentes UI con clases utilitarias | Utility-first en templates, `@apply` en SCSS, componentes Card/Alert/Badge con Tailwind |
| [capitulo30-parte3.md](capitulo30-parte3.md) | Responsive design y Dark Mode con Tailwind | Breakpoints `sm:/md:/lg:`, `darkMode: 'class'`, toggle con Signal, `prefers-color-scheme` |
| [capitulo30-parte4.md](capitulo30-parte4.md) | Tailwind + Angular Material: convivencia armoniosa | Desactivar preflight, `@layer`, estrategia híbrida Material+Tailwind para proyectos reales |
| [capitulo31-parte1.md](capitulo31-parte1.md) | Testing unitario con Jest: setup y primeras pruebas | Migrar de Karma a Jest, `jest-preset-angular`, `TestBed`, primer test de componente standalone |
| [capitulo31-parte2.md](capitulo31-parte2.md) | Testing de componentes con Angular Testing Library | `render()`, `screen.getByRole()`, `userEvent`, filosofía de testing por comportamiento |
| [capitulo31-parte3.md](capitulo31-parte3.md) | Testing de servicios, HTTP y NgRx | `HttpTestingController`, `MockStore`, `overrideSelector`, testing de effects |
| [capitulo31-parte4.md](capitulo31-parte4.md) | E2E Testing con Playwright en proyectos Angular | `playwright.config.ts`, queries accesibles, Page Object Model, CI con GitHub Actions |

---

### PARTE XIV — Arquitectura y Patrones Avanzados
*Capítulos 32–35 · 16 archivos*

Patrones de arquitectura escalable, micro-frontends con Module Federation y Native Federation, internacionalización, accesibilidad avanzada y despliegue en producción.

| Archivo | Título | Descripción breve |
|---|---|---|
| [capitulo32-parte1.md](capitulo32-parte1.md) | Arquitectura por features y dominios escalables | Feature-based structure, barrel exports con `index.ts`, separación UI/dominio |
| [capitulo32-parte2.md](capitulo32-parte2.md) | Smart Components y Dumb Components | Container vs Presentational, reglas para cada tipo, relación con OnPush y testing |
| [capitulo32-parte3.md](capitulo32-parte3.md) | Facade Pattern con servicios y NgRx | `ProductosFacade` que abstrae el store, ventajas en testing, cuándo es overhead |
| [capitulo32-parte4.md](capitulo32-parte4.md) | Nx Workspace: monorepos y arquitectura de librerías | `create-nx-workspace`, tagging de librerías, `nx affected:test`, `enforce-module-boundaries` |
| [capitulo33-parte1.md](capitulo33-parte1.md) | ¿Qué son los micro-frontends y cuándo usarlos? | Motivación, patrones de composición (client-side/server-side), cuándo NO usar MFE |
| [capitulo33-parte2.md](capitulo33-parte2.md) | Webpack Module Federation con Angular | Host y remote con `@angular-architects/module-federation`, `shared`, versioning |
| [capitulo33-parte3.md](capitulo33-parte3.md) | Native Federation: Module Federation sin Webpack | Import Maps nativos, `federation.config.js`, `initFederation()` en `main.ts`, comparativa |
| [capitulo33-parte4.md](capitulo33-parte4.md) | Comunicación entre micro-frontends: eventos y estado compartido | Custom Events, `BroadcastChannel`, shell como mediador de autenticación, qué NO compartir |
| [capitulo34-parte1.md](capitulo34-parte1.md) | i18n nativo con @angular/localize | Atributo `i18n`, `ng extract-i18n`, XLIFF, `ng build --localize`, un build por locale |
| [capitulo34-parte2.md](capitulo34-parte2.md) | Transloco: la alternativa moderna para i18n en runtime | `@jsverse/transloco`, JSON de traducciones, cambio de idioma sin recargar, lazy loading |
| [capitulo34-parte3.md](capitulo34-parte3.md) | Accesibilidad (a11y): semántica, roles ARIA y Angular | HTML semántico, `aria-label`, `aria-live`, gestión del foco en SPAs |
| [capitulo34-parte4.md](capitulo34-parte4.md) | Patrones ARIA avanzados y auditoría de accesibilidad | Dialog/Combobox/Tabs accesibles, `axe-core` en tests, Lighthouse en CI |
| [capitulo35-parte1.md](capitulo35-parte1.md) | Configuración de entornos: environment.ts y variables de entorno | `fileReplacements`, `APP_CONFIG` con `InjectionToken`, config en runtime con `APP_INITIALIZER` |
| [capitulo35-parte2.md](capitulo35-parte2.md) | CI/CD con GitHub Actions: build, test y deploy automático | Workflow YAML completo, caché de `node_modules`, deploy a GitHub Pages/Firebase/Vercel |
| [capitulo35-parte3.md](capitulo35-parte3.md) | Dockerización de apps Angular y deploy en cloud | Dockerfile multi-stage, `nginx.conf` para SPA, Cloud Run y ECS Fargate |
| [capitulo35-parte4.md](capitulo35-parte4.md) | Monitoreo, error tracking con Sentry y analytics | `@sentry/angular`, `ErrorHandler`, GA4 con consent management, GDPR |

---

### PARTE XV — Angular 20 y el Futuro del Framework
*Capítulo 36 · 4 archivos*

Las novedades estables de Angular 20: `@let` en templates, signal-based queries, `linkedSignal()` y `resource()` estables, hydratación incremental, modos de renderizado por ruta, HMR mejorado, y el roadmap hacia Angular 21 con Zoneless estable y Signal Forms.

| Archivo | Título | Descripción breve |
|---|---|---|
| [capitulo36-parte1.md](capitulo36-parte1.md) | `@let` en templates y signal-based queries | Declaración de variables locales reactivas, `viewChild()`/`contentChild()` como Signals |
| [capitulo36-parte2.md](capitulo36-parte2.md) | linkedSignal(), resource() y httpResource() en Angular 20 | APIs promovidas a developer preview/estable, comparativa con enfoques anteriores |
| [capitulo36-parte3.md](capitulo36-parte3.md) | Hydratación incremental y modos de renderizado por ruta | `withIncrementalHydration()`, `@defer hydrate on`, `RenderMode` por ruta en `app.routes.server.ts` |
| [capitulo36-parte4.md](capitulo36-parte4.md) | Zoneless, Angular 21 y el roadmap del framework | `provideZonelessChangeDetection()` estable, Signal Forms, `@angular/build`, hoja de ruta |

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
