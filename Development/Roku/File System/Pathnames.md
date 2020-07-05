# Pathnames

A Roku Streaming Player Pathname identifies a file. Pathnames are used in methods, as well as in other components which use files. A Pathname is a string with the following format:

``` 
device:/dir1/dir2/…/filename
  
```

The device field (sometimes called PHY) identifies the location of the
file and can be one of:

  - **tmp** - Temporary file storage device for the application
  - **pkg** - The root of the application directory that provides
    read-only access to files provided in the pkg
  - **common** – A common read-only filesystem that all plugins have
    access to. Currently, it only contains a CA certificate bundle that
    contains CA certs trusted by FireFox
    ([common:/certs/ca-bundle.crt](http://common/certs/ca-bundle.crt)).
    You are encouraged to use this file in your apps, especially if you
    are aggregating many different feeds. Please see the twitterOAuth
    sample application for a usage example.
  - **ext1, ext2, …,ext9** – Storage devices recognized on the USB bus.
    Please see the USB player sample application for a usage example.

There is no concept of a current working directory or relative paths.
All path names **must** use the absolute Roku Streaming Player Pathname
format above.

The filename components in a pathname may not contain any of these
characters:

``` 
  <  >  :  "  /  |  ?  *
  
```

nor any whitespace or non-printable character.

## Example

**Example of path names used from BrightScript**

``` 
theme.OverhangSliceSD = "pkg:/images/Overhang_Slice_SD43.png"
  
  http.Http.GetToFile("tmp:/categorylist")
  
  DeleteFile("tmp:/categorylist")
  
  obj.SetCertificatesFile("common:/certs/ca-bundle.crt")
  
```

