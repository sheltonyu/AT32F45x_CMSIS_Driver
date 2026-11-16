from building import *
import os

cwd = GetCurrentDir()

path = [cwd]
src = ['system_at32f45x.c']

if rtconfig.PLATFORM in ['gcc', 'llvm-arm']:
    src += [os.path.join('startup', 'gcc', 'startup_at32f45x.s')]
elif rtconfig.PLATFORM in ['armcc', 'armclang']:
    src += [os.path.join('startup', 'mdk', 'startup_at32f45x.s')]
elif rtconfig.PLATFORM in ['iccarm']:
    src += [os.path.join('startup', 'iar', 'startup_at32f45x.s')]

group = DefineGroup('cmsis', src, depend = ['PKG_USING_AT32F45x_CMSIS_DRIVER'], CPPPATH = path)

Return('group')
