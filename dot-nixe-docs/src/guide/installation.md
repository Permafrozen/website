# Installation

<div class="warning">

If you install this config on a VM, make sure to enable `hardware-acceleration`. Also, change the GRUB boot settings to use the appropriate device, e.g., `"/dev/sda"`.

</div>

## Five Step Installation

1. Add experimental features to `configuration.nix`:
    ```nix
    nix.settings.experimental-features = [ "nix-command" "flakes" ];
    ```

2. Rebuild your system to apply changes:
    ```bash
    sudo nixos-rebuild switch
    ```

3. Clone the repository (in ~):
    ```bash
    git clone https://github.com/Permafrozen/dot-nixe .dot-nixe
    ```

4. Copy your `/etc/nixos/hardware-configuration.nix` to the host you want to use (the default host is `laptop`):
    ```bash
    cp /etc/nixos/hardware-configuration.nix ~/.dot-nixe/hosts/laptop
    ```

5. Rebuild with the flake *(inside the dot-nixe directory)*:
    ```bash
    sudo nixos-rebuild switch --flake .
    ```
