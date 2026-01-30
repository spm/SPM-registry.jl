# SPM-registry.jl
Local registry for Julia pakages use by SPM

## Usage
To use this registry, the following needs to be done once:
```
using Pkg
pkg"registry add https://github.com/spm/SPM-registry.jl"
```
This will create a ``$JULIA_DEPOT_PATH/registries/SPM`` folder that shows where to obtain various unregistered packages used by SPM.
 
## More information
Entries to the registry can be created using the `LocalRegistry` package, which can be installed by:
```
using Pkg
Pkg.add("LocalRegistry")
```
The `SPM` local registry was made by first creating an empty git repo at `https://github.com/spm/SPM-registry.jl`, and typing the following in Julia:
```
using LocalRegistry
create_registry("SPM", "https://github.com/spm/SPM-registry.jl"; push = true)
```

An entry to the local registry can be added using (e.g.):
```
using LocalRegistry
using PushPull
register(PushPull)
```

For more about using local registries, see 
https://github.com/GunnarFarneback/LocalRegistry.jl .
