## 1.0.0-beta.8

* Added fields to support formatted errors and logs.
  * `CompileFailure.formatted`
  * `LogEvent.formatted`
  * `CompileRequest.color`

* Remove `OutputStyle.NESTED` and `OutputStyle.COMPACT`. It's unlikely that any
  host would support those any time soon.

## 1.0.0-beta.7

* Use `4294967295` as the special ID for error messages that aren't caused by a
  specific request, since `-1` isn't representable as a `uint32`.

## 1.0.0-beta.6

* Changed `CompileResponse.id` and `ProtocolError.id` from `int32` to `uint32`
  to match the type of all other ID fields.

* Added protocol versions and created this changelog.

* Added the `VersionRequest` and `VersionResponse` messages.

* Delimit messages with varints rather than fixed-size integers.
