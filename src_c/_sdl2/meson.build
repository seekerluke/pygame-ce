cython_base = '../cython/pygame/_sdl2'

_sdl2_audio = shared_module(
    'audio',
    fs.is_file('audio.c') ? 'audio.c' : cython_base / 'audio.pyx',
    dependencies: pg_base_deps,
    include_directories: ['..'],
    install_dir: pg / '_sdl2',
)

_sdl2_video = shared_module(
    'video',
    fs.is_file('video.c') ? 'video.c' : cython_base / 'video.pyx',
    dependencies: pg_base_deps,
    include_directories: ['..'],
    install_dir: pg / '_sdl2',
)

_sdl2_controller_old = shared_module(
    'controller_old',
    fs.is_file('controller_old.c') ? 'controller_old.c' : cython_base / 'controller_old.pyx',
    dependencies: pg_base_deps,
    include_directories: ['..'],
    install_dir: pg / '_sdl2',
)

if sdl_mixer_dep.found()
    _sdl2_mixer = shared_module(
        'mixer',
        fs.is_file('mixer.c') ? 'mixer.c' : cython_base / 'mixer.pyx',
        dependencies: pg_base_deps + sdl_mixer_dep,
        include_directories: ['..'],
        install_dir: pg / '_sdl2',
    )
endif

_sdl2_sdl2 = shared_module(
    'sdl2',
    fs.is_file('sdl2.c') ? 'sdl2.c' : cython_base / 'sdl2.pyx',
    dependencies: pg_base_deps,
    include_directories: ['..'],
    install_dir: pg / '_sdl2',
)

# This is not a cython file
_sdl2_touch = shared_module(
    'touch',
    'touch.c',
    dependencies: pg_base_deps,
    include_directories: ['..'],
    install_dir: pg / '_sdl2',
)

_sdl2_controller = shared_module(
    'controller',
    'controller.c',
    dependencies: pg_base_deps,
    include_directories: ['..'],
    install_dir: pg / '_sdl2',
)
