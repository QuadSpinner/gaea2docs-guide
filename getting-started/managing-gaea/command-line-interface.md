---
icon: sparkles
---

# Command-line Interface

Gaea provides two command line interfaces. One for the UI and for the Build Swarm.

## Gaea.exe

You can use the CLI for [activation.md](../license-management/activation.md "mention") and [deactivation.md](../license-management/deactivation.md "mention") as well as setting the Proxy, or enforcing [cpu-only-mode.md](../../troubleshooting/diagnostics-watson/cpu-only-mode.md "mention") or enabling Verbose logging for detailed diagnostics.

```sh
USAGE: 
Gaea [[-Path] <String>] [-Activate <String>] [-CPUOnly] [-Deactivate] [-Help] 
     [-NoStart] [-Proxy <String>] [-SafeMode] [-UseProxy] [-Verbose] [-Version]

    -Path <String>
        The path of the file to read.

    -Activate <String>
        Activate license. Default value: <empty>.

    -CPUOnly [<Boolean>]
        Disable GPU/XPU acceleration, defaulting to CPU-only mode.
        Default value: False.

    -Deactivate [<Boolean>]
        Deactivate license. Default value: False.

    -Help [<Boolean>] (-?, -h)
        Displays this help message.

    -NoStart [<Boolean>]
        Disable Start Screen Default value: False.

    -Proxy <String>
        Set Proxy for all network communications. Default value: <empty>.

    -SafeMode [<Boolean>]
        Enforce Safe Mode. Default value: False.

    -UseProxy [<Boolean>]
        Use Proxy for all network communications.

    -Verbose [<Boolean>]
        Enable Verbose logging for diagnostics and technical usage purposes.
        Default value: False.

    -Version [<Boolean>]
        Displays version information.

```

## Gaea.Swarm.exe

For the Build Swarm, see [command-line-automation.md](../../advanced-topics/automation/command-line-automation.md "mention").

```sh
USAGE:
Gaea.Swarm [[--Filename] <String>] [--ignorecache] [--interactive] [-p <String>] 
           [-r <String>] [--safemode] [--seed <Int32>] 
           [-v <String=String>...] [--va <String>...] [--vars <String>] [--verbose]

OPTIONS:
  --Filename <string>
      REQUIRED. Relative or absolute path to the terrain file to build.

  --ignorecache               
      Force Build Swarm to ignore Baked Cache.
  
  --interactive               
      Show interactive prompts when launched from the CLI.
  
  -p|--profile <string>       
      Build Profile to use when executing the Build.
  
  -r|--region <string>        
      Set the Region that should be built.
  
  --safemode                  
      Enforce Safe Mode.
  
  --seed <int32>              
      Mutation seed to use for the build.
  
  -v|--v <string=string>      
      Repeat in key-value pairs to assign variables. Ex: -v foo:0.63.
                              
  --va <string>               
      Comma separated variable values alphanumerically-sorted by variable names. 
      Must include all values.
                              
  --vars <string>             
      Fully qualified path to a .json or .txt file that
      contains variable name-value pairs for automation.
                              
  --verbose                   
      Enable Verbose logging for diagnostics and technical usage purposes.

```
