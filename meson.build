project('MyLib', 'cpp', default_options : ['cpp_std=c++14'])

install_headers(['MyLib/MyLib.hpp'],
	subdir: 'MyLib'
)

incDirs = include_directories('.')

lib = library('Tink', 
        ['MyLib/MyLib.cpp'],
        include_directories : incDirs,
        install: true)

exe = executable('HelloWorld',
	sources: ['main.cpp'],
	include_directories: incDirs,
	link_with: lib,
	install: true,
)
