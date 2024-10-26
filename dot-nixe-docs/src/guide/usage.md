# Usage

## Rebuilding with `nh`

<div class="warning">

Remeber to be inside the same directory if you use `.`

</div>

```bash
nh os switch .
```

## Rebuilding without `nh`


<div class="warning">

Remeber to be inside the same directory if you use `.`

</div>

```bash
sudo nixos-rebuild switch --flake .
```

## Updating your flake

<div class="warning">

You have to rebuild to use the updated configuration.

</div>

```bash
nix flake update
```