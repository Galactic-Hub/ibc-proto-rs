- Re-export the `ics23.cosmos.v1` Protobuf definitions from the `ics23` crate instead of including them directly in this crate.
  The proto definitions are exported both under the `ibc_proto::cosmos::ics23::v1` module and under the `ibc_proto::ics23` module
  for backward source compatiblity. This is nonetheless a breaking change as it may break compilation or trigger warnings
  in code which relied on these definitions being different than the ones in `ics23`.
  ([\#10](https://github.com/cosmos/ibc-proto-rs/issues/10))