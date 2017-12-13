# Toyota Connected: Elixir Guild
## Property Testing
#### 2017-12-13 &mdash; Andrew Bennett <[andrew.bennett@toyotaconnected.com](mailto:andrew.bennett@toyotaconnected.com)>

##### Property Testing Frameworks

* [`eqc_ex`](https://github.com/Quviq/eqc_ex) &mdash; uses [`eqc`](http://quviq.com/documentation/eqc/) (commercial, full version requires license)
* [`propcheck`](https://github.com/alfert/propcheck) &mdash; uses [`PropEr`](https://github.com/manopapad/proper) (GPLv3)
* [`excheck`](https://github.com/parroty/excheck) &mdash; uses [`triq`](https://github.com/triqng/triq) (Apache 2.0)

##### (Partial) Property Testing Frameworks

* [`stream_data`](https://github.com/whatyouhide/stream_data) &mdash; developed by [@whatyouhide](https://github.com/whatyouhide) and [@josevalim](https://github.com/josevalim) (incomplete, very light on features)
* [`quixir`](https://github.com/pragdave/quixir) &mdash; uses [`pollution`](https://github.com/pragdave/pollution) for stream generation (incomplete)

##### Getting Started (`eqc`)

Add the following to your `mix.exs`:

```elixir
{:eqc_ex, "~> 1.4", only: :test}
```

Run the following to install eqcmini (free version):

```bash
MIX_ENV=test mix eqc.install --mini
```

Add `use EQC.ExUnit` to your test module and then use `property "..." do` to write your property tests.

See the [`eqc_ex` docs](https://hexdocs.pm/eqc_ex/) and the [`eqc` docs](http://quviq.com/documentation/eqc/) for more information.

##### Getting Started (`PropEr`)

Add the following to your `mix.exs`:

```elixir
{:propcheck, "~> 1.0", only: :test}
```

Add `use PropCheck` to your test module and then use `property "..." do` to write your property tests.

See the [`propcheck` docs](https://hexdocs.pm/propcheck/), [`PropEr` documentation](http://proper.softlab.ntua.gr/), and [Fred Hebert's book &ldquo;PropEr Testing&rdquo;](https://propertesting.com/) for more information.

##### Getting Started (`triq`)

Add the following to your `mix.exs`:

```elixir
{:excheck, "~> 0.5", only: :test},
{:triq, github: "triqng/triq", only: :test}
```

Add the following to your `test_helper.exs`:

```elixir
ExCheck.start()
```

Add `use ExCheck ` to your test module and then use `property "..." do` to write your property tests.

See the [`excheck` docs](https://hexdocs.pm/excheck/) or the [`triq` project page](https://github.com/triqng/triq) for more information.

##### Learning Resources

* [Testing Web Services with QuickCheck (Thomas Arts, 2017)](https://www.youtube.com/watch?v=dDDCSDTHRZo)
* [PropEr Testing (Fred Hebert, 2017)](https://propertesting.com/)
* [QuickCheck: A Lightweight Tool for Random Testing of Haskell Programs (John Hughes, 2000)](http://www.cs.tufts.edu/~nr/cs257/archive/john-hughes/quick.pdf)

##### Other Resources

* [QuickCheck on Wikipedia](https://en.wikipedia.org/wiki/QuickCheck)
* [QuickCheck CI](http://quickcheck-ci.com/)
