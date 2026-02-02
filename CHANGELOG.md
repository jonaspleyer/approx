## 0.6.0
Version `0.6.0` includes PRs which have been opened over the course of many years.
As such it accumulates a lot of changes at once.
This version aims to be backwards-compatible, i.e. by explicitly utilizing the existing test-suite,
and only extending previous tests.
However due to the large amount of changes, a new major release was chosen.

- Implementations for more types
    - `Option<T>`
    - `Result<T>`
    - Arrays `[T; N]` (activated by default with `array_impl` feature)
    - Tuples `(T,)`, `(T,T)`, up to size `11` (activated by default with `tuple_impl` feature)
    - `Vec<T>` (requires `vec_impl` feature and `extern alloc` crate)
    - `NotNan` and `OrderedFloat` (requires `ordered_float` feature)
    - `u128` and `i128`
    - `Complex` of the `num-complex` crate (requires `num_complex` feature)
    - `indexmap` (requires `indexmap_impl` feature)
- Derive macros for `AbsDiffEq` and `RelativeEq`
    - requires `derive` feature
    - will lead to increased compile times since crates such as `syn` and `proc-macro2` are required
- Updated dependencies
- Update edition
- Added tests for all new features
- Extended CI

## pre 0.5.1
There has not been a concise effort to provide a changelog prior to versions including `0.5.1`.
