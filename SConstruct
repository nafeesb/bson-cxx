import glob, os

env = Environment()
name = 'bsoncxx'
srcs = Glob('src/bson/*.cpp')

env.Append( CPPPATH=['/usr/local/include'] )

lib = env.StaticLibrary( name, srcs )
env.Install( '#install/lib', lib )
env.Install( '#install/include', Glob('src/bson/*.h') )

env.Append(LIBPATH = ['#install/lib'])
env.Append(LIBS=[lib])

env.Install('#install/bin', env.Program('example1', 'src/examples/example1.cpp'))
