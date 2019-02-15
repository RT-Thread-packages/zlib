# RT-Thread building script for zlib

from building import *

# get current directory
cwd = GetCurrentDir()

zlib_inc = cwd + '/inc'
zlib_src = cwd + '/src'

src = Glob(zlib_src + '/*.c')

if GetDepend('ZLIB_USING_SAMPLE'):
    src += Glob('zlib_sample.c')

CPPPATH = [zlib_inc]

group = DefineGroup('zlib', src, depend = ['PKG_USING_ZLIB'], CPPPATH = CPPPATH)

Return('group')
