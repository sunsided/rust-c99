## stdint

Provides C99 integer types such as `uint_fast16_t`, `uint_least16_t` etc. for interfacing with
C libraries that use them.

### Types of defined sizes

| N    | Exact size (N bits)   | Smallest type with at least N bits | Fastest type with at least N bits |
|------|-----------------------|------------------------------------|-----------------------------------|
| `8`  | `int8_t`, `uint8_t`   | `int_least8_t`, `uint_least8_t`    | `int_fast8_t`, `uint_fast8_t`     |
| `16` | `int16_t`, `uint16_t` | `int_least16_t`, `uint_least16_t`  | `int_fast16_t`, `uint_fast16_t`   |
| `32` | `int32_t`, `uint32_t` | `int_least32_t`, `uint_least32_t`  | `int_fast32_t`, `uint_fast32_t`   |
| `64` | `int64_t`, `uint64_t` | `int_least64_t`, `uint_least64_t`  | `int_fast64_t`, `uint_fast64_t`   |

## Special types

| Type                    | Purpose                         |
|-------------------------|---------------------------------|
| `intptr_t`, `uintptr_t` | Type capable of holding `*void` |
| `intmax_t`, `uintmax_t` | Largest integer type available  |

### Constants

According `MIN` and `MAX` constants defined in `stdint.h` are exposed through
the `consts` module such as `INT_FAST16_MIN` and `INT_FAST16_MAX`. Due to Rust's type system,
these value are identical to `int_fast16_t::MIN` and `int_fast16_t::MAX`.
