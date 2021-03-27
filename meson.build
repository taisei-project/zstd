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
    # There shouldn't be any need to force a C standard convention for zstd
    # but in case one would want that anyway, this can be done here.
    # 'c_std=gnu99',
    # c++11 standard is useful for pzstd
    'cpp_std=c++11',
    'buildtype=release',
    'warning_level=3',
    # -Wdocumentation does not actually pass, nor do the test binaries,
    # so this isn't safe
    #'werror=true'
  ],
  version: run_command(
    find_program('build/meson/GetZstdLibraryVersion.py', native : true),
    join_paths(meson.current_source_dir(), 'lib/zstd.h')
  ).stdout().strip(),
  meson_version: '>=0.50.0')

subdir('build/meson')
