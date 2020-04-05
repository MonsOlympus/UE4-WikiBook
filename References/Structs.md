# Structs

Structs (or structures) are a composite [data type](https://en.wikipedia.org/wiki/Data_type) that can contain multiple [member variables](https://en.wikipedia.org/wiki/Member_variable), including another struct type.

*Structures in C++ can have member functions along with data members.*

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
- USTRUCT()
Without this declaration the struct type is a basic C++ struct type. However when delcared as used with the parameter BlueprintType this becomes a managed object usable with UE4s Blueprint Editor.
- GENERATED_BODY()
- UPROPERTY()

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
