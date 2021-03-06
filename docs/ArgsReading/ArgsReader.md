# ArgsReader class

Helps process command-line arguments.

```csharp
public sealed class ArgsReader
```

## Public Members

| name | description |
| --- | --- |
| [ArgsReader](ArgsReader/ArgsReader.md)(…) | Creates a reader for the specified command-line arguments. |
| [LongOptionIgnoreCase](ArgsReader/LongOptionIgnoreCase.md) { get; set; } | True if long options (e.g. `--help`) should ignore case. (Default false.) |
| [LongOptionIgnoreKebabCase](ArgsReader/LongOptionIgnoreKebabCase.md) { get; set; } | True if long options (e.g. `--dry-run`) should ignore "kebab case", i.e. allow `--dryrun`. (Default false.) |
| [NoOptionsAfterDoubleDash](ArgsReader/NoOptionsAfterDoubleDash.md) { get; set; } | True if `--` is ignored and all following arguments are not read as options. (Default false.) |
| [ShortOptionIgnoreCase](ArgsReader/ShortOptionIgnoreCase.md) { get; set; } | True if short options (e.g. `-h`) should ignore case. (Default false.) |
| [ReadArgument](ArgsReader/ReadArgument.md)() | Reads the next non-option argument. |
| [ReadArguments](ArgsReader/ReadArguments.md)() | Reads any remaining non-option arguments. |
| [ReadFlag](ArgsReader/ReadFlag.md)(…) | Reads the specified flag, returning true if it is found. |
| [ReadOption](ArgsReader/ReadOption.md)(…) | Reads the value of the specified option, if any. |
| [VerifyComplete](ArgsReader/VerifyComplete.md)() | Confirms that all arguments were processed. |

## Remarks

To use this class, construct an `ArgsReader` with the command-line arguments from `Main`, read the supported options one at a time with [`ReadFlag`](ArgsReader/ReadFlag.md) and [`ReadOption`](ArgsReader/ReadOption.md), read any normal arguments with [`ReadArgument`](ArgsReader/ReadArgument.md), and finally call [`VerifyComplete`](ArgsReader/VerifyComplete.md), which throws an [`ArgsReaderException`](ArgsReaderException.md) if any unsupported options or arguments haven't been read.

## See Also

* namespace [ArgsReading](../ArgsReading.md)
* [ArgsReader.cs](https://github.com/ejball/ArgsReading/tree/master/src/ArgsReading/ArgsReader.cs)

<!-- DO NOT EDIT: generated by xmldocmd for ArgsReading.dll -->
