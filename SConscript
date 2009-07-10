#
# SConscript for GPSDisplay base directory
#
# $Id: SConscript,v 1.2 2009/07/10 20:30:46 avr Exp $
#

Import('env')

# libserial library
#
env.Append(LIBSERIALDIR = '/usr/local')
env.Append(LIBSERIALINCDIR = env['LIBSERIALDIR'] + '/include')
env.Append(LIBSERIALLIBDIR = env['LIBSERIALDIR'] + '/lib')
env.Append(LIBSERIALLIB = 'serial')

# some more build options
#
#env.AppendUnique(CPPDEFINES = ['APRS'])
env.AppendUnique(CCFLAGS= ['-std=c99'])
env.AppendUnique(CPPPATH = [ env['LIBSERIALINCDIR'] ])
env.AppendUnique(LIBPATH = [ env['LIBSERIALLIBDIR'] ])

# program gpstest
#
srcs = Split('gpstest.cc LcdDisplay.c GPS.c ui.c')

env.Program('gpstest', srcs, LIBS = env['LIBSERIALLIB'])

# --- eof