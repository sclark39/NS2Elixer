#Elixer
#### Cross-Mod Compatible Utility Function Library for Modders

Put ```Elixer_Utility.lua``` in a **unique** subdirectory of your mod to avoid any conflicts. If the file path matches any other mod's, the results will be unpredictable.

Call ```Elixer.UseVersion( versionNumber )``` before trying to call any of these functions in your mod to ensure the right versions are loaded into memory

### To Use
```
Script.Load( "lua/youruniquesubdir/Elixer_Utility.lua" )
Elixer.UseVersion( 1.71 )
```

### Included Functions
```lua
-- Function List
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
AppendToEnum( tbl, key )
list ( ... )
set( tbl )
```

### Latest changes
- 2014-07-06:
	- Released first version of Elixer to the community