# ~50 State Management Libraries & Frameworks

You can manage your state with React [local state (setState)](https://reactjs.org/docs/state-and-lifecycle.html#adding-local-state-to-a-class), [hooks](https://reactjs.org/docs/hooks-intro.html) and [context](https://reactjs.org/docs/context.html), but often that's not ideal for complex applications. So far the most common choice for state management there has been Redux, but there are many other alternatives. Inspired by various posts about the state of state management in JavaScript, we decided to compile a thorough list of options and compare them in the categories we care about.

Explanation of columns:

- **GitHub stars** - we're using this as a rough measure of popularity. We know it's not perfect, and it might become out of date with time. We also considered using NPM downloads, GitHub "used by" or watchers, etc., but this was the simplest way to start.
- **TypeScript support** - we care about TypeScript. Most libraries that offer good support for it will mention it in their README or docs, and that's what we looked at to fill this column.
- **Performance** - we didn't run and test performance for all of these, so this is also based on what they say in their documentation. Other people have benchmarked different frameworks, for example [here](https://krausest.github.io/js-framework-benchmark/current.html).
- **API Complexity** - the APIs vary from simple and easy to learn, to complex and full of boilerplate. At the moment this field will often link to the API documentation that you can check for yourself, but we are working on filling it in more directly. For now, we're adding a couple broad categories: simple, medium and complex. These are a little bit subjective, so let us know if you disagree.
- **Abstract Concepts** - this is a list of concepts you'll need to learn to use this framework.
- **Extensibility** - how easy is it to customize and extend the framework with either middleware, plugins or otherwise?
- **Devtools** - does the framework come with its own developer tools, loggers, or integrate with existing (usually Redux) developer tools?
- **Time travel** - do the devtools offer time travel functionality? If you're not familiar with this, you can check the Redux example [here](https://medium.com/the-web-tub/time-travel-in-react-redux-apps-using-the-redux-devtools-5e94eba5e7c0)).
- **Automation** - TBD

This table is roughly ordered by number of GitHub stars, but we’ve also grouped some related libraries together, for example different MobX variations.
If any field is enclosed in "double quotes", it's a quote taken directly from their README or docs.

To see how Prodo compares, see our [README](https://github.com/prodo-dev/prodo).

## Contributions

There's a lot of information to keep track of here, so it's entirely possible we got something wrong, or it went out of date. If you spot a mistake, or want to add a new entry to the table, please make a PR! We welcome comments and suggestions.

## Comparison Table

Compiled in October 2019. A version of this page with a table you can filter is [here](https://prodo-dev.github.io/state-management/).

| Framework/Library | Notes | Link | GitHub Stars | TypeScript support | Performance | API Complexity | Abstract concepts | Extensibility | Devtools | Time travel | Automation |
| - | - | - | - | - | - | - | - | - | - | - | - |
| Redux | | https://github.com/reduxjs/redux (https://github.com/reduxjs/react-redux) | 51k (18.2k) | https://redux.js.org/recipes/usage-with-typescript#usage-with-typescript (yes, but adds a fair bit of boilerplate/effort) | https://redux.js.org/faq/performance | Complex (https://redux.js.org/api/api-reference) | actions, action creators, reducers, store, dispatch, thunk, saga, observable… | Middleware | https://github.com/reduxjs/redux-devtools | yes | |
| MobX | | https://github.com/mobxjs/mobx (https://github.com/mobxjs/mobx-react) | 20.7k (3.9k) | not mentioned | Not discussed much in docs; a bit worse than Redux in https://krausest.github.io/js-framework-benchmark/current.html (looking at react-mobx, not mobx-jsx) | Complex (https://mobx.js.org/refguide/api.html) | decorators, observable state, computed values, reactions, actions | not mentioned | https://github.com/mobxjs/mobx-devtools | no | |
| MobX State Tree | different from MobX | https://github.com/mobxjs/mobx-state-tree | 4.8k | “Typescript typings are included in the packages.” | "If you have a performance critical application that handles a huge amount of mutable data, you will probably be better off by using 'raw' MobX…” | Complex (https://github.com/mobxjs/mobx-state-tree#api-overview) | tree, node, type, state, model, actions, views | https://github.com/mobxjs/mobx-state-tree/blob/master/docs/middleware.md | Supports MobX DevTools, Reactotron or Redux | yes | |
| Parket | heavily isnpired by mobx-state-tree, but smaller | https://github.com/ForsakenHarmony/parket | 408 | not mentioned | not mentioned | Medium? _(heavily inspired by mobx-state-tree, but smaller)_ | proxies, symbols, decorators, observe, connect, unistore | not mentioned | no | no | |
| Remx | opinionated MobX | https://github.com/wix/remx | 113 | not mentioned | talks about MobX but not specifically this library | Relatively simple (https://github.com/wix/remx#api) | implements redux (flux) architecture in MobX, state, getters, setters, connect | no | maybe MobX? + logger/debugger | no | |
| Unstated | | https://github.com/jamiebuilds/unstated | 6.9k | not mentioned much, some types exist | not mentioned | “Simple” | container, subscribe, provider | not mentioned | debugger: https://github.com/sindresorhus/unstated-debug | no | |
| Unstated-next | | https://github.com/jamiebuilds/unstated-next | 1.5k | written in typescript | Claims to be faster than Redux in the docs | Based on hooks, so should be easy to learn | container, hooks | not mentioned | no? | no | |
| Constate | hooks + context | https://github.com/diegohaz/constate | 2.1k | has an example | not mentioned | Simple (https://github.com/diegohaz/constate#api) | hooks, context | not mentioned | no | no | |
| Unistore | | https://github.com/developit/unistore | 2.6k | not mentioned | not mentioned | Simple (https://github.com/developit/unistore#api) | store, actions | not mentioned | Supports Redux devtools extension | ? | |
| Stockroom | Unistore in a worker | https://github.com/developit/stockroom | 1.6k | not mentioned | not mentioned much (performance demo) | Simple (https://github.com/developit/stockroom#api) | unistore, worker, stockroom module | not mentioned | no (although can use Redux devtools extension for Unistore?) | no | |
| React Copy Write | | https://github.com/aweary/react-copy-write | 1.8k | not mentioned | not mentioned | Simple | immer, immutable state, mutate, optimized selector | not mentioned | no | no | |
| Redux Zero | | https://github.com/redux-zero/redux-zero | 1.8k | https://github.com/redux-zero/redux-zero#typescript | not mentioned | Simple | store, actions, no reducers | https://github.com/redux-zero/redux-zero#middleware | Yes + integrates with Redux DevTools | ? | |
| Fr(e)actal | | https://github.com/FormidableLabs/freactal | 1.7k | not mentioned | not mentioned | Medium (https://github.com/FormidableLabs/freactal#api-documentation) | provideState, injectState, effects, intermediate state, computed values, multiple states | not mentioned | no | no | |
| Easy React State | | https://github.com/solkimicreb/react-easy-state | 1.6k | not mentioned | "It performs a bit better than MobX and similarly to Redux.” (https://github.com/krausest/js-framework-benchmark) | Simple | store, view | not mentioned | no | no | |
| Reworm | | https://github.com/pedronauck/reworm | 1.4k | has typings | not mentioned | Simple https://github.com/pedronauck/reworm) | provider, get & set, selector, subscribe | not mentioned | no | no | |
| Undux | | https://github.com/bcherny/undux | 1.3k | “Complete type-safety, no exceptions” | not mentioned | Simple (get, set) | store, container, effects, subscriptions = Rx observables | Plugins | Logger + Supports Redux DevTools extension | yes | |
| Microstates | composable state primitives | https://github.com/microstates/microstates.js/ (https://github.com/microstates/react) | 1.3k (45) | (different composable / transpilation free type system) | not mentioned | Medium - complex | microstates, transitions, state machines | not mentioned | no | no | |
| Apollo Link State | now in Apollo Client core | https://github.com/apollographql/apollo-link-state  | 1.4k | Apollo provides tools to generate types | | | Medium (https://www.apollographql.com/docs/link/links/state/)| | https://github.com/apollographql/apollo-client-devtools | no | |
| React automata + setState | | https://github.com/MicheleBertoli/react-automata | 1.2k | not mentioned | not mentioned | Simple - medium (https://github.com/MicheleBertoli/react-automata#api) | state machines, xstate, transition, Action, State | not mentioned | Can connect to Redux DevTools Extension (if using with Redux?) | ? | |
| Storeon | | https://github.com/storeon/storeon | 1.1k | "Storeon delivers TypeScript declaration which allows to declare type of state and optionally declare types of events and parameter."| "Fast. It tracks what parts of state were changed and re-renders only components based on the changes." | Simple - medium | store, events, init, dispatch, changed, hooks - useStoreon, connect | not mentioned | Logger + "supports debugging with Redux DevTools Extension" | no | |
| Overmind | | https://github.com/cerebral/overmind | 680 | "Overmind is written in Typescript and it is written with a focus on you dedicating as little time as possible to help Typescript understand what your app is all about.” | (they don’t talk about perfomance much) | Medium (https://overmindjs.org/api/action?view=react&typescript=false) | state, actions, effects, operators | not mentioned | yes | no | |
| Dob | | https://github.com/dobjs/dob | 651 | not mentioned | not mentioned | Simple - medium | proxy, decorators: observable, inject, Connect, Action | not mentioned | https://github.com/dobjs/dob-react-devtools (also can bind to redux?) | no | |
| Statty | | https://github.com/vesparny/statty | 519 | not mentioned | not mentioned | Simple (https://github.com/vesparny/statty) | Provider, State, selector, updater | not mentioned | no | no | |
| SatchelJS | to use with React, add MobX | https://github.com/Microsoft/satcheljs | 339 | Written in TypeScript, examples assume it | “Satchel enables a very performant UI, only rerendering the minimal amount necessary. MobX makes UI updates very efficient by automatically detecting specifically what components need to rerender for a given state change.” | Medium | store, observer decorator, action creator, dispatch, murator, orchestrator, mutatorAction | not mentioned | maybe MobX? | no | |
| ReComponent | reducer components | https://github.com/philipp-spiess/react-recomponent | 269 | “Comes with TypeScript definitions built-in.” | not mentioned | Relatively simple (https://github.com/philipp-spiess/react-recomponent#api-reference) | reducer components, effects | not mentioned | no | no | |
| React Recollect | similar to react-easy-state | https://github.com/davidgilbertson/react-recollect | 250 | https://github.com/davidgilbertson/react-recollect#usage-with-typescript | not mentioned | Medium (https://github.com/davidgilbertson/react-recollect#api) | immutable store, collect, selector, updater | not mentioned | debugger | no | |
| Controllerim | | https://github.com/Niryo/controllerim | 196 | not mentioned | “Controllerim utilizes Mobx behind the scenes for all the performance boosts (Memoizes values, calculates dependencies and renders only when trully needed)” | Simple - medium (https://github.com/Niryo/controllerim#api) | controller, observer | not mentioned | maybe MobX? | no | |
| Laco | | https://github.com/deamme/laco | 162 | not mentioned | not mentioned | Medium (https://github.com/deamme/laco#api, inspired by redux and unstated) | inferno, store, actions, subscribe | | Partially supports Redux devTools and React Native debugger | yes | |
| Reatom | | https://github.com/artalar/reatom | 147 | "static typed: best type inferences" | "performant updates for partial state changes" | Medium - complex (https://artalar.github.io/reatom/#/faq?id=why-is-api-so-strange-can39t-it-be-simpler) | atom, action, store, dispatch, subscribe, observable,  | | no | no | |
| Pure Store | | https://github.com/gunn/pure-store | 102 | “It also works excellently with typescript.” | not mentioned | “Simple” | store, update, subscribe | not mentioned | no | no | |
| Tiny Atom | | https://github.com/KidkArolis/tiny-atom | 90 | not mentioned | “highly optimised with batched rerenders” | “tiny api - easy to understand, easy to adapt” (https://kidkarolis.github.io/tiny-atom/api-reference/) | atom, actions, async actions, connect, provider, consumer, updater, | custom `evolve` hook | Logger + Redux DevTools integration | | |
| Alfa | | https://github.com/lsm/alfa | 80 | not mentioned | “Fast – Alfa wraps your components with a thin layer. It introduces little to no performance impacts.” | “Only 4 functions/APIs to learn” (https://lsm.github.io/alfa/#/?id=api) | inject, subscribe, provide, actions, dynamic keys, store | not mentioned | no | no | |
| Reim | | https://github.com/IniZio/reim | 79 | “Typing support for Typescript & Flow” | not mentioned | Simple - medium | immer, immutable state, store, snapshot, actions, State | not mentioned | Supports Redux Dev Tools | ? | |
| React Recontext | | https://github.com/minhtc/react-recontext | 78 | not mentioned | not mentioned | Simple (https://github.com/minhtc/react-recontext#api) | store, provider, actions, action creators, connect, dispatch | not mentioned | Logger | no | |
| Pullstate | | https://github.com/lostpebble/pullstate | 75 | "Built with Typescript, providing a great dev experience if you're using it too.” | not mentioned | Simple | store, update, subscriptions, reactions, async actions, immer | not mentioned | no | no | |
| Prodo | | https://github.com/prodo-dev/prodo | 67 | "First class support for TypeScript" | "Blazingly fast re-rendering" | "Absolutely minimal boilerplate" | model, store, watch, dispatch, actions | https://docs.prodo.dev/basics/plugins/ | https://docs.prodo.dev/basics/devtools/ | WIP | TBD |
| Dakpan | | https://github.com/houfio/dakpan | 64 | “TypeScript types come bundled” | not mentioned | Relatively simple (https://dakpan.houf.io/usage.html) | hooks, actions | not mentioned | no | no | |
| Hookstate | | https://github.com/avkonst/hookstate | 44 | "First-class Typescript support. Complete type inferrence for any complexity of structures of managed state data. Full intellisense support tested in VS Code.” | “Incredible performance based on unique method for tracking of used/rendered and updated state segments.” (https://hookstate.netlify.com/performance-demo-large-table …) | Medium | global, local and scoped state | https://github.com/avkonst/hookstate#plugins | no | no | |
| ClearX | | https://github.com/Autodesk/clearx | 40 | not mentioned | not mentioned | "ClearX has a familiar API." (https://github.com/Autodesk/clearx#api) | store, paths, | not mentioned | no | no | |
| Refnux | | https://github.com/algesten/refnux | 36 | not mentioned | not mentioned | Simple - medium | like redux but functions instead of reducers | not mentioned | no | no | |
| Stator | | https://github.com/cs01/stator | 26 | not mentioned | not mentioned | “Intuitive, Small API: Similar to React's, with no boilerplate necessary” https://github.com/cs01/stator | store, subscriptions | Middleware | no | no | |
| Hez | | https://github.com/linq2js/hez | 21 | not mentioned | not mentioned | Medium | store, actions, hooks | not mentioned | no | no | |
| Sunfish | | https://github.com/tzilist/Sunfish | 17 | not mentioned | “Updating React can be expensive. Updates to state only happen when the developer deems it necessary.” | "Sunfish has a fairly intuitive, functionaly driven api." (https://github.com/tzilist/Sunfish#api) | transaction, pipe | not mentioned | no | no | |
| Elfi | | https://github.com/madx/elfi | 16 | not mentioned | not mentioned | Simple | store, dispatch, subscribe | Middleware | Logger | no | |

Some other state-related libraries that haven't made it into the table:

- [baobab](https://github.com/Yomguithereal/baobab)
- [cycle-onionify](https://github.com/staltz/cycle-onionify)
- [freezer](https://github.com/arqex/freezer)
- [jetemit](https://github.com/uxitten/jetemit)
- [jumpsuit](https://github.com/jsonmaur/jumpsuit) (deprecated)
- [microstate](https://github.com/estrattonbailey/microstate) (archived)
- [reactObservableStore](https://github.com/taviroquai/ReactObservableStore)
- [react-contextual](https://github.com/drcmda/react-contextual)
- [react-refetch](https://github.com/heroku/react-refetch)
- [react-simplified](https://gitlab.com/eidheim/react-simplified)
- [ReduxX](https://github.com/msteckyefantis/reduxx) (taken down)
- [redux-lightweight](https://github.com/doniyor2109/redux-lightweight)
- [rematch](https://github.com/rematch/rematch)
- [rosmaro](https://rosmaro.js.org/)
