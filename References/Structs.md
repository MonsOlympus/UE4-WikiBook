# Structs

Structs (or structures) are a composite [data type](https://en.wikipedia.org/wiki/Data_type) that allow programmers to group members into a single type. A struct (in C++) can contain any combination of [member variables](https://en.wikipedia.org/wiki/Member_variable) including other struct types and [member functions](https://en.wikipedia.org/wiki/Method_(computer_programming)#Member_functions_in_C++).

However this does not extend to Blueprint, structs created within the Unreal Editor are limited to member variables only as member functions cannot be declared with the UFUNCTION Macro.

## Declaration Syntax

```c++
USTRUCT(BlueprintType)
struct FYourStructName
{
    GENERATED_BODY()
    
public:
    UPROPERTY()
    int32 YourMemberVariable;
};
```

All Structs in Unreal Engine 4 are prefixed with a *capital F* this is a form of [Hungarian Notation](https://en.wikipedia.org/wiki/Hungarian_notation) Epic uses to identify certain types within their engine.

For a full list of prefixes used within the UE4 C++ code: ...

### UE4 Macros
These [macros](https://github.com/MonsOlympus/UE4-WikiBook/blob/master/References/Macros.md) are a way for Unreal Engine 4 to manage these as objects.
##### USTRUCT()
Without this declaration the struct is a standard C++ struct type. However when delcared as used with the parameter BlueprintType this becomes a managed object usable with UE4s Blueprint Editor.
##### UPROPERTY()
For a member variable to be considered for replication it must use the UPROPERTY() macro.
##### UFUNCTION()
Should not be used with Struct Member Functions!

### Struct Constructors and Default Member Variables
There are a few different ways of defining default member variables for structs.

```c++
USTRUCT(BlueprintType)
struct FYourStructName
{
    GENERATED_BODY()
    
public:
    UPROPERTY()
    int32 YourMemberVariable;
    
    FYourStructName()
    {
        YourMemberVariable = 10;
    }
};
```
```c++
USTRUCT(BlueprintType)
struct FLimitedResource
{
	GENERATED_BODY()

	UPROPERTY()
	FName Name;

	UPROPERTY()
	FVector Value;

	FLimitedResource()
		: Name("Default"), Value(FVector(0.0f, 0.0f, 0.0f))
	{}

	FLimitedResource(const FName NewName, const FVector NewValue)
		: Name(NewName), Value(NewValue)
	{}
};
```

This is the most basic, using the default constructor to set the member variable once it is created.

## Nesting Structs
When nesting structs it is important that the struct you wish to use as a member variable be delcared, you may want to seperate our your most use structs to a header which can be reused in many files.

```c++
USTRUCT(BlueprintType)
struct FYourFirstStructName
{
    GENERATED_BODY()
    
public:
    UPROPERTY()
    int32 YourMemberVariable;
};

USTRUCT(BlueprintType)
struct FYourSecondStructName
{
    GENERATED_BODY()
    
public:
    UPROPERTY()
    FYourFirstStructName YourStructMemberVariable;
};
```

## Extending Structs

```c++
USTRUCT(BlueprintType)
struct FYourFirstStructName
{
    GENERATED_BODY()
    
public:
    UPROPERTY()
    int32 YourMemberVariable;
};

USTRUCT(BlueprintType)
struct FYourSecondStructName : public FYourFirstStructName
{
    GENERATED_BODY()
    
};
```
Inherits YourMemberVariable from the parent Struct in the same way Class inheritance works.

## Struct Assignment

## Accessing Struct Members

### Nested Structs

## Initialising Structs

## Further Reading
- [Official - Unreal Architecture - Structs](https://docs.unrealengine.com/en-US/Programming/UnrealArchitecture/Reference/Structs/index.html)
- [Wikipedia - C Programming - Structs](https://en.wikipedia.org/wiki/Struct_(C_programming_language))

Back to [Main Page](../README.md)