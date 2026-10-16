# LECmd

## Command Line Interface

    LECmd version 1.4.0.0
    
    Author: Eric Zimmerman (saericzimmerman@gmail.com)
    https://github.com/EricZimmerman/LECmd
    
            d               Directory to recursively process. Either this or -f is required
            f               File to process. Either this or -d is required
            q               Only show the filename being processed vs all output. Useful to speed up exporting to json and/or csv. Default is FALSE
    
            r               Only process lnk files pointing to removable drives. Default is FALSE
            all             Process all files in directory vs. only files matching *.lnk. Default is FALSE
    
            csv             Directory to save CSV formatted results to. Be sure to include the full path in double quotes
            csvf            File name to save CSV formatted results to. When present, overrides default name
    
            xml             Directory to save XML formatted results to. Be sure to include the full path in double quotes
            html            Directory to save xhtml formatted results to. Be sure to include the full path in double quotes
            json            Directory to save json representation to. Use --pretty for a more human readable layout
            jsonf           File name to save JSON formatted results to. When present, overrides default name
            pretty          When exporting to json, use a more human readable layout. Default is FALSE
    
            nid             Suppress Target ID list details from being displayed. Default is FALSE
            neb             Suppress Extra blocks information from being displayed. Default is FALSE
    
            dt              The custom date/time format to use when displaying time stamps. See https://goo.gl/CNVq0k for options. Default is: yyyy-MM-dd HH:mm:ss
            mp              Display higher precision for time stamps. Default is FALSE
    
    Examples: LECmd.exe -f "C:\Temp\foobar.lnk"
              LECmd.exe -f "C:\Temp\somelink.lnk" --json "D:\jsonOutput" --pretty
              LECmd.exe -d "C:\Temp" --json "D:\jsonOutput" --jsonf results.json -q
              LECmd.exe -d "C:\Temp" --csv "c:\temp" --html c:\temp --xml c:\temp\xml -q
              LECmd.exe -f "C:\Temp\some other link.lnk" --nid --neb
              LECmd.exe -d "C:\Temp" --all
    
              Short options (single letter) are prefixed with a single dash. Long commands are prefixed with two dashes    

`--jsonf` overrides the filename of the single JSON results file written to the
`--json` directory, for both `-f` and `-d`. Any directory component in `--jsonf`
is discarded, and the supplied extension is preserved without adding `.json`.
Without `--json`, `--jsonf` is ignored. Existing output files are overwritten.
Without `--jsonf`, the filename remains `yyyyMMddHHmmss_LECmd_Output.json`.

CSV and JSON output paths must be different. LECmd compares their full paths
without case sensitivity and reports an error before opening any export files
if they match.

## Documentation

LNK Explorer Command Line edition!

[Introducing LECmd!](https://binaryforay.blogspot.com/2016/02/introducing-lecmd.html)

[LECmd v0.6.0.0 released!](https://binaryforay.blogspot.com/2016/02/lecmd-v0600-released.html)

[PECmd, LECmd, and JLECmd updated!](https://binaryforay.blogspot.com/2016/03/pecmd-lecmd-and-jlecmd-updated.html)

[LECmd and JLECmd updated](https://binaryforay.blogspot.com/2016/04/lecmd-and-jlecmd-updated.html)

# Download Eric Zimmerman's Tools

All of Eric Zimmerman's tools can be downloaded [here](https://ericzimmerman.github.io/#!index.md). 

# Special Thanks

Open Source Development funding and support provided by the following contributors: [SANS Institute](http://sans.org/) and [SANS DFIR](http://dfir.sans.org/).
