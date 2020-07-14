07_13_2020
---------------------


07_12_2020
---------------------
cd C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans
dotnet.exe run -p .\FSharpKoans\FSharpKoans.fsproj


        let result = add add 5 8 add 1 1

PS C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans> dotnet.exe run -p .\FSharpKoans\FSharpKoans.fsproj
C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\AboutTheOrderOfEvaluation.fs(19,26): error FS0001: Type mismatch. Expecting a    ''a'    but given a    ''a -> 'b -> 'c -> 'd -> 'e
 -> 'f -> 'g'    The types ''a' and ''a -> 'b -> 'c -> 'd -> 'e -> 'f -> 'g' cannot be unified. [C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\FSharpKoans.fsproj]
C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\AboutTheOrderOfEvaluation.fs(19,34): error FS0001: Type mismatch. Expecting a    ''a'    but given a    ''b -> int -> int -> 'a -> 
'c -> 'd -> 'e'    The types ''a' and ''b -> int -> int -> 'a -> 'c -> 'd -> 'e' cannot be unified. [C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\FSharpKoans.fsproj]
C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\AboutTheOrderOfEvaluation.fs(17,15): error FS0043: The type 'int -> 'a -> int -> int -> 'b' does not match the type 'int' [C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\FSharpKoans.fsproj]

The build failed. Fix the build errors and run again.


right order:


        let result = add (add 5 8) (add 1 1)

        let result = double <| add 5 8

        Backward pipes are cool!




https://www.javatpoint.com/f-sharp-return-multiple-values-using-tuples#:~:text=F%23%20Return%20Multiple%20Values%20Using,multiple%20values%20by%20using%20tuples.
F# Return Multiple Values Using Tuples
Function does not return multiple values. In F#, you can return multiple values by using tuples. Let's see an Example.

let TupleExample a b =   
 let c = a+b  
 let d = a-b  
 (c, d)  
   
let tupleValues = TupleExample 50 10   
printf "%A" tupleValues  
Output:

(60, 40)

        let message = printf "F# turns it to %d!" 11

PS C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans> dotnet.exe run -p .\FSharpKoans\FSharpKoans.fsproj
C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\AboutStrings.fs(29,32): error FS0001: This expression was expected to have type    'unit'    but here has type    'string' [C:\User
s\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\FSharpKoans.fsproj]

The build failed. Fix the build errors and run again.

      let message = sprintf "F# turns it to %d!" "one"

PS C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans> dotnet.exe run -p .\FSharpKoans\FSharpKoans.fsproj
C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\AboutStrings.fs(27,52): error FS0001: The type 'string' is not compatible with any of the types byte,int16,int32,int64,sbyte,uint16,uint32,uint64,nativeint,unativeint, arising from the use of a printf-style format string [C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\FSharpKoans.fsproj]

The build failed. Fix the build errors and run again.
PS C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans> 

07_07_2020
---------------------

https://dotnet.microsoft.com/download/dotnet-core/thank-you/runtime-3.1.5-windows-x64-installer


https://dotnet.microsoft.com/download/dotnet-core/sdk-for-vs-code?utm_source=vs-code&amp;utm_medium=referral&amp;utm_campaign=sdk-install

Forked the project to be able to push to my github

Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

Transcript started, output file is C:\Users\tcailleau\Documents\WindowsPowerShell\PSTranscript\PSTranscript7_7_2020.txt
Date: 7/7/2020
Time: 8:12 PM
Loading personal and system profiles took 1341ms.
PS C:\Users\tcailleau\Documents\WindowsPowerShell\Scripts> dotnet build
Microsoft (R) Build Engine version 16.6.0+5ff7b0c9e for .NET Core
Copyright (C) Microsoft Corporation. All rights reserved.

MSBUILD : error MSB1003: Specify a project or solution file. The current working directory does not contain a project or solution file.
PS C:\Users\tcailleau\Documents\WindowsPowerShell\Scripts> cd C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans
PS C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans> dotnet build
Microsoft (R) Build Engine version 16.6.0+5ff7b0c9e for .NET Core
Copyright (C) Microsoft Corporation. All rights reserved.

  Determining projects to restore...
  Restored C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans.Test\FSharpKoans.Test.fsproj (in 12.59 sec).
  FSharpKoans.Core -> C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans.Core\bin\Debug\netstandard2.0\FSharpKoans.Core.dll
  FSharpKoans.Test -> C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans.Test\bin\Debug\netcoreapp3.1\FSharpKoans.Test.dll
  FSharpKoans -> C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\bin\Debug\netcoreapp3.1\FSharpKoans.dll

Build succeeded.
    0 Warning(s)
    0 Error(s)
PS C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans> dotnet.exe run -p .\FSharpKoans\FSharpKoans.fsproj


about asserts:
    AssertExpectation failed.



You have not yet reached enlightenment ...
Seek wisdom by filling in the __

Please meditate on the following code:
   at FSharpKoans.about asserts.AssertExpectation() in C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\AboutAsserts.fs:line 30




Press any key to continue...

PS C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans> dotnet.exe run -p .\FSharpKoans\FSharpKoans.fsproj


about asserts:
    AssertExpectation passed
    FillInValues passed

about let:
    LetBindsANameToAValue failed.



You have not yet reached enlightenment ...
Seek wisdom by filling in the __

Please meditate on the following code:
   at FSharpKoans.about let.LetBindsANameToAValue() in C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\AboutLet.fs:line 18




Press any key to continue...

PS C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans> dotnet.exe run -p .\FSharpKoans\FSharpKoans.fsproj


about asserts:
    AssertExpectation passed
    FillInValues passed

about let:
    LetInfersTheTypesOfValuesWherePossible passed
    YouCanMakeTypesExplicit passed
    FloatsAndInts passed
    ModifyingTheValueOfVariables passed



You have not yet reached enlightenment ...
  Expected: 100
  But was:  50


Please meditate on the following code:
   at NUnit.Framework.Assert.ReportFailure(String message)
   at NUnit.Framework.Assert.ReportFailure(ConstraintResult result, String message, Object[] args)
   at NUnit.Framework.Assert.That[TActual](TActual actual, IResolveConstraint expression, String message, Object[] args)
   at NUnit.Framework.Assert.AreEqual(Object expected, Object actual)
   at FSharpKoans.about let.YouCannotModifyALetBoundValueIfItIsNotMutable() in C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\AboutLet.fs:line 85




PS C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans> dotnet.exe run -p .\FSharpKoans\FSharpKoans.fsproj
C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\AboutLet.fs(79,9): error FS0027: This value is not mutable. Consider using the mutable keyword, e.g. 'let mutable x = expression'. [C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\FSharpKoans.fsproj]

The build failed. Fix the build errors and run again.
PS C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans> dotnet.exe run -p .\FSharpKoans\FSharpKoans.fsproj


about asserts:
    AssertExpectation passed
    FillInValues passed

about let:
    LetBindsANameToAValue passed
    LetInfersTheTypesOfValuesWherePossible passed
    YouCanMakeTypesExplicit passed
    FloatsAndInts passed
    ModifyingTheValueOfVariables passed
    YouCannotModifyALetBoundValueIfItIsNotMutable passed

about functions:
    CreatingFunctionsWithLet failed.



You have not yet reached enlightenment ...
Seek wisdom by filling in the __

Please meditate on the following code:
   at FSharpKoans.about functions.CreatingFunctionsWithLet() in C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\AboutFunctions.fs:line 27




Press any key to continue...

PS C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans> dotnet.exe run -p .\FSharpKoans\FSharpKoans.fsproj
C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\AboutFunctions.fs(48,13): error FS0072: Lookup on object of indeterminate type based on information prior to this program point. A type annotation may be needed prior to this program point to constrain the type of the object. This may allow the lookup to be resolved. [C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\FSharpKoans.fsproj]

The build failed. Fix the build errors and run again.
PS C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans> 

Now adding type annotation back makes the test pass -----------------------------------------

about functions:
    CreatingFunctionsWithLet passed
    NestingFunctions passed
    AddingTypeAnnotations passed
    VariablesInTheParentScopeCanBeAccessed failed.



You have not yet reached enlightenment ...
Seek wisdom by filling in the __

Please meditate on the following code:
   at FSharpKoans.about functions.VariablesInTheParentScopeCanBeAccessed() in C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\AboutFunctions.fs:line 66




Press any key to continue...

Still Learning -----------------------------------------

about functions:
    CreatingFunctionsWithLet passed
    NestingFunctions passed
    AddingTypeAnnotations passed
    VariablesInTheParentScopeCanBeAccessed failed.



You have not yet reached enlightenment ...
  Expected string length 14 but was 19. Strings differ at index 0.
  Expected: "HELLO THERE!!!"
  But was:  "hellothere!!!YELLED"
  -----------^

  Completed VariablesInTheParentScopeCanBeAccessed -----------------------------------------


about functions:
    CreatingFunctionsWithLet passed
    NestingFunctions passed
    AddingTypeAnnotations passed
    VariablesInTheParentScopeCanBeAccessed passed

about the order of evaluation:
    SometimesYouNeedParenthesisToGroupThings failed.



You have not yet reached enlightenment ...
Seek wisdom by filling in the __

Please meditate on the following code:
   at FSharpKoans.about the order of evaluation.SometimesYouNeedParenthesisToGroupThings() in C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\AboutTheOrderOfEvaluation.fs:line 21





Please meditate on the following code:
   at NUnit.Framework.Assert.ReportFailure(String message)
   at NUnit.Framework.Assert.ReportFailure(ConstraintResult result, String message, Object[] args)
   at NUnit.Framework.Assert.That[TActual](TActual actual, IResolveConstraint expression, String message, Object[] args)
   at NUnit.Framework.Assert.AreEqual(Object expected, Object actual)
   at FSharpKoans.about functions.VariablesInTheParentScopeCanBeAccessed() in C:\Users\tcailleau\Documents\NETCore3.1\FSharp\FSharpKoans\FSharpKoans\AboutFunctions.fs:line 66



