# vue3-axios

Composition API & Vue component helpers for making API requests and rendering the results in vue 3

## summary

The library offers 3 different layers of abstraction for making API requests that can be used separately:

1. `useAPI` is a hook that can be used in any component and gives the user full control of the request (cancellation, caching, refetch, error & loading states)
2. `AxiosComponent` is an Async component that uses the `useAPI` hook to render/mount itself only when the initial request is done and the results are ready. it delegates rendering of error / loading or results via named slots.
3. `VueAxiosComponent` Which uses `AxiosComponent` to provide generic error & loading states and uses the new `Suspense` API to handle rendering of the Async Component. it delegates rendering of results via a named slot.
