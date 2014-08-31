#Elixer
#### Cross-Mod Compatible Utility Library for Modders


### To Use

Put ```Elixer_Utility.lua``` in a **unique** subdirectory of your mod to avoid any conflicts. If the file path matches any other mod's, the results will be unpredictable.

```
Script.Load( "lua/youruniquesubdir/Elixer_Utility.lua" )
Elixer.UseVersion( 1.8 )
```

You should also call ```Elixer.UseVersion( versionNumber )``` before trying to call any of these functions in your mod to ensure the right versions are loaded into memory


### Included Functions
```lua
-- Function List
Elixer.UseVersion( versionNumber )
EPrint( fmt, ... )
EPrintDebug( fmt, ... )
EPrintCallHook( class, name )
Class_AddMethod( className, methodName, method )
upvalues( func )
PrintUpValues( func )
GetUpValue( func, upname, options )
LocateUpValue( func, upname, options )
SetUpValues( func, source )
CopyUpValues( dst, src )
ReplaceUpValue( func, localname, newval, options )
locals( stacklevel )
GetLocalsFromCallingFunction()
SetLocalFromCallingFunction( localname, newval )
AppendToEnum( tbl, key )
list ( ... )
set( tbl )
```

### Latest changes
- 2014-08-31: (Version 1.8)
	- Added locals(stacklevel) iterator
	- Added GetLocalsFromCallingFunction() which returns a table with name/value pairs of the calling functions
	- Added SetLocalFromCallingFunction( localname, newval ) to overwrite the value of a local in a calling function
	
- 2014-06-10: (Version 1.72)
	- Fixed Class_AddMethod to assert instead of silently fail if the method already exists in the class
	- Fixed prints not showing the full version number
	
- 2014-06-07: (Version 1.71)
	- Released first version of Elixer to the community