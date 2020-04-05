# Structs

Structs (or structures) are a composite [data type](https://en.wikipedia.org/wiki/Data_type) that allow programmers to group members into a single type. A struct (in C++) can contain any combination of [member variables](https://en.wikipedia.org/wiki/Member_variable) including other Struct types and [member functions](https://en.wikipedia.org/wiki/Method_(computer_programming)#Member_functions_in_C++).

However this does not extend to Blueprint, Structs created within the Unreal Editor are limited to member variables only as member functions cannot be declared with the UFUNCTION Macro.

## Declaration Syntax

```C++
USTRUCT(BlueprintType)
struct FYourStructName
{
    GENERATED_BODY()
    
public:
    UPROPERTY()
    int32 YourMemberVariable;
};
```

### UE4 Macros
These macros are a way for Unreal Engine 4 to manage these as objects.
##### USTRUCT()
Without this declaration the struct is a standard C++ struct type. However when delcared as used with the parameter BlueprintType this becomes a managed object usable with UE4s Blueprint Editor.
##### GENERATED_BODY()
##### UPROPERTY()
##### UFUNCTION()
Should not be used with Struct Member Functions!

### Struct Constructors and Default Member Variables
There are a few different ways of defining default member variables for structs.

```C++
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
This is the most basic, using the default constructor to set the member variable once it is created.

## Nesting Structs

## Struct Assignment

## Accessing Struct Members

## Initialising Structs

## Further Reading
- [Official - Unreal Architecture - Structs](https://docs.unrealengine.com/en-US/Programming/UnrealArchitecture/Reference/Structs/index.html)
- [Wikipedia - C Programming - Structs](https://en.wikipedia.org/wiki/Struct_(C_programming_language))
