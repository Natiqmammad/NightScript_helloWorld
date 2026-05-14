# NightScript Hello World (AFNS)

Bu layihə NightScript (`.afns`) üçün ən sadə `Hello World` nümunəsidir.

## Layihə Quruluşu

```text
hello_world_afns/
├── night.toml
└── src/
    └── main.afns
```

## Kod

`src/main.afns` faylı:

```afns
package main;

extern "C" fn puts(s: cstr) -> i32;

fn main() -> i32 {
    puts("Hello World from NightScript!");
    return 0;
}
```

## Necə İşlətmək Olar

NightScript kompilyatoru bu repodadır:

`/mnt/zboth/ApexForge_NightScript/compiler/build/night`

### 1) Sintaksis Yoxlaması

```bash
/mnt/zboth/ApexForge_NightScript/compiler/build/night check src/main.afns
```

### 2) Build

```bash
/mnt/zboth/ApexForge_NightScript/compiler/build/night build src/main.afns -o hello_world_afns
```

### 3) Run

```bash
/mnt/zboth/ApexForge_NightScript/compiler/build/night run src/main.afns -o hello_world_afns
```

Uğurlu nəticə:

```text
Hello World from NightScript!
```
