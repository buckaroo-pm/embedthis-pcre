macos_headers = {
  'me.h': 'projects/pcre-macosx-default-me.h',
}

linux_headers = {
  'me.h': 'projects/pcre-linux-default-me.h',
}

cxx_library(
  name = 'pcre',
  header_namespace = '',
  exported_headers = {
    'pcre.h': 'src/pcre.h', 
  }, 
  headers = subdir_glob([
    ('src', '**/*.h'),
  ]),
  platform_headers = [
    ('macos.*', macos_headers),
    ('linux.*', linux_headers),
  ],
  srcs = glob([
    'src/**/*.c',
  ]),
  visibility = [
    'PUBLIC',
  ],
)
