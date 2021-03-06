# mqtt-packet [![Build Status](https://travis-ci.org/toddtreece/mqtt-packet.svg?branch=master)](https://travis-ci.org/toddtreece/mqtt-packet) [![codecov](https://codecov.io/gh/toddtreece/mqtt-packet/branch/master/graph/badge.svg)](https://codecov.io/gh/toddtreece/mqtt-packet) [![Crates.io](https://img.shields.io/crates/v/mqtt-packet.svg)](https://crates.io/crates/mqtt-packet)

A [MQTT v5.0][mqtt] packet parser and generator written in [Rust][rust]. This crate is primarily a learning project, and is unstable due to active development.

Some of the goals of this project are:
* Write a parser/generator using only the [MQTT v5.0 specification][mqtt] as a reference.
* Do not reference any existing MQTT libraries in any language during development.
* Avoid using external dependencies if possible.
* Keep up with test coverage and documentation during development.
* Avoid using heap, i.e., [String] and [Vec]. This should make it easier to use in embedded clients.
  * *Update:* This one is on hold for the MVP. v2.0 will likely need to support the [no_std]
  environment to work on , so this is going to be a larger effort than removing `String` and `Vec`.
  I don't currently have time to refactor the existing code, and for the MVP done is better than perfect. 
* Probably some other stuff that I have forgotten...

## License
Copyright (c) 2019 Todd Treece. Licensed under the MIT license.

[mqtt]: https://docs.oasis-open.org/mqtt/mqtt/v5.0/os/mqtt-v5.0-os.html
[rust]: https://www.rust-lang.org/
[String]: https://doc.rust-lang.org/std/string/struct.String.html
[Vec]: https://doc.rust-lang.org/std/vec/struct.Vec.html
[no_std]: https://rust-embedded.github.io/book/intro/no-std.html