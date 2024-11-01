## Changelog

### V2.0.4

#### Non-Breaking Changes

- Added new PVC labels - Thank you ohnoitsyou 

### V2.0.3

#### Non-Breaking Changes

- Updated Chart test to wait for the service to become available before testing rcon port

### V2.0.2

#### Non-Breaking Changes

- Updated version of the factorio badge to 2.0.10

### V2.0.1

#### Non-Breaking Changes

- Added `enable_space_age` field to values.yaml to enable or disable Space Age DLC

### V2.0.0

#### Breaking Changes

Now compatible only with Factorio V2.0.
The Space Age DLC is not required to use this Helm chart.
Some Factorio settings in general have changed.
To continue using older 'factoriotools/factorio' Docker images, use version V1.2.5.

- Updated fields in values.yaml for Factorio V2.0 and Space Age DLC.

### V1.2.0

#### Non-Breaking Changes

- Added `securityContext` field to values.yaml

### V1.1.2

#### Non-Breaking Changes

- Fixed a bug where the `game-password` volume had an invalid name

### V1.1.1

#### Non-Breaking Changes

- Fixed a bug where the `account-data` volume had an invalid name
- Extended the pod's DNS config to ensure correct DNS resolution in certain
  environments

### V1.1.0

#### Breaking Changes

- Moved account data from `server_settings.` to `account.` in values.yaml
- Moved server password from `server_settings.` to `serverPassword.` in values.yaml

#### Non-Breaking Changes

- Added `account.accountSecret` field to values.yaml
- Added `rcon.passwordSecret` field to values.yaml
- Added `serverPassword.passwordSecret` field to values.yaml
- Changed default `rcon.password` to `CHANGEMECHANGEME`, which should be changed anyway
- Changed default `map_gen_settings.autoplace_controls` from the standard values to `{}`, since by default map
  generation follows standard parameters if not overriden
- Changed default `admin_list`, `white_list` and `ban_list` to `[]` instead of `nil`
