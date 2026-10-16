# LECmd

LECmd examines Windows shortcut artifacts and exports the evidence they contain.

## Language

**LNK file**:
A Windows shortcut artifact containing information about a target and the context in which the shortcut was created or used.
_Avoid_: Target file (when referring to the shortcut itself)

**Source file**:
The LNK file being examined by LECmd.
_Avoid_: Target

**Target**:
The file, directory or other resource referenced by a LNK file. The target may no longer exist when the shortcut is examined.
_Avoid_: Source file
