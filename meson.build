# #############################################################################
# Copyright (c) 2018-present     Dima Krasner <dima@dimakrasner.com>
#                                lzutao <taolzu(at)gmail.com>
# All rights reserved.
#
# This source code is licensed under both the BSD-style license (found in the
# LICENSE file in the root directory of this source tree) and the GPLv2 (found
# in the COPYING file in the root directory of this source tree).
# #############################################################################

project('zstd',
  ['c', 'cpp'],
  license: ['BSD', 'GPLv2'],
  default_options : [
    'c_std=gnu99',
    'cpp_std=c++11',
    'buildtype=release'
  ],
  version: run_command(
    find_program('build/meson/GetZstdLibraryVersion.py', native : true),
    join_paths(meson.current_source_dir(), 'lib/zstd.h')
  ).stdout().strip(),
  meson_version: '>=0.47.0')


subdir('build/meson')
