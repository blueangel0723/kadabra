# Changelog

## v0.3.6
- Fixed: ES flag properly set on certain HEADERS frames

## v0.3.5
- Fixed: Memory leak on connection crashes
- New supervision structure. `Kadabra.open/2` now returns a supervisor pid,
  but the API for making requests remains unchanged.

## v0.3.4
- Fixed: Connections properly respect settings updates

## v0.3.3
- Fixed: Hpack memory leak on connection close

## v0.3.2
- Fixed: Connection settings defaults are now actually default

## v0.3.1
- Fixed: Sending payloads larger than the stream window

## v0.3.0
- Minimum requirements are now Elixir 1.4/OTP 19
- Performance improvements for individual streams
- Fixed: multiple connections now supported per host
- Request responses now return with new `%Stream.Response{}` struct
- Push promises can be intercepted with `{:push_promise, %Stream.Response{}}`
  messages

## v0.2.2
- `Connection` now respects `max_concurrent_streams`
- Fixed: proper WINDOW_UPDATE responses on received DATA frames

## v0.2.1
- Fixed: calling `Kadabra.open/3` with `reconnect: false` to disable
  automatic reconnect on socket close
