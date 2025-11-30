
```bash
# Get path to "ping" executable
which ping
```

```bash
# Get capabilities for "ping" executable
getcap $(which ping)
```

```bash
# Set `cat_ne_raw` capability to "ping" executable with value 'ep'
sudo setcap cap_net_raw=ep $(which ping)
```

##### Nix
- `nix store gc`

##### NixOS
- `sudo /run/current-system/specialisation/gaming/activate
`
