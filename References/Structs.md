# Structs

Structs (or structures) are a composite [data type](https://en.wikipedia.org/wiki/Data_type) that can contain multiple [member variables](https://en.wikipedia.org/wiki/Member_variable), including another struct type.

## Declaration Syntax

```C++
USTRUCT(BlueprintType)
struct FYourStructName
{
    GENERATED_BODY()
    
public:
  int32 YourMemberVariable;
};
```

### UE4 Macros
- USTRUCT()
- GENERATED_BODY()
- UPROPERTY()

### Struct Constructors and Default Member Variables

## Further Reading
- [Official - Unreal Architecture - Structs](https://docs.unrealengine.com/en-US/Programming/UnrealArchitecture/Reference/Structs/index.html)
- [Wikipedia - C Programming - Structs](https://en.wikipedia.org/wiki/Struct_(C_programming_language))
