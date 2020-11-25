project('PROJECT_NAME',
	['c', 'cpp'],
	default_options : [
		'warning_level=3',
		'werror=false',
		# This project defaults to a release build
		'debug=false',
		'optimization=2',
		# `build.*` options affect `native: true targets`
		# plain options affect `native: false` targets.
		'c_std=c11', 'build.c_std=c11',
		'cpp_std=c++17', 'build.cpp_std=c++17',
	],
	meson_version: '>=0.56.0',
	version: '0.1'
)

nucleo_l4r5zi_subproject = subproject('nucleo_l4r5zi')
nucleo_l4r5zi_dep = nucleo_l4r5zi_subproject.get_variable('nucleo_l4r5zi_demo_platform_dep')
host_map_file = nucleo_l4r5zi_subproject.get_variable('host_map_file')
host_hex_conversion = nucleo_l4r5zi_subproject.get_variable('host_hex_conversion')
host_bin_conversion = nucleo_l4r5zi_subproject.get_variable('host_bin_conversion')

desired_common_compile_flags = nucleo_l4r5zi_subproject.get_variable('desired_common_compile_flags')
desired_cpp_compile_flags = nucleo_l4r5zi_subproject.get_variable('desired_cpp_compile_flags')
desired_native_cpp_compile_flags = nucleo_l4r5zi_subproject.get_variable('desired_native_cpp_compile_flags')

subdir('src')
