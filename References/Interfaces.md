# Interfaces
Interfaces in Unreal Engine are an extremely useful tool though I feel they are underused because of the difficulty with implementation. This isnt a standard feature of C++ so the compiler does always give you a nice error message.

## Interface Declaration
Header
```c++
UINTERFACE()
class UYourInterface : public UInterface
{
    GENERATED_BODY()
};
```
Class
```C++
class PROJECT_API IYourInterface
{
    GENERATED_BODY()

    // Add interface functions to this class. This is the class that will be inherited to implement this interface.
public:


    virtual bool InterfaceFunction(SomeType* const TypePtr, const float& SomeFloat, const TArray<FText>& SomeTextEntries);
};
```
/* Actor header (override declaration): */
```C++
class PROJECT_API AMyActor : public AActor, public IMyInterface

virtual bool InterfaceFunction(SomeType* const TypePtr, const float& SomeFloat, const TArray<FText>& SomeTextEntries);
```
/* Actor source (override definition): */
```C++
bool AMyActor::InterfaceFunction(SomeType* const TypePtr, const float& SomeFloat, const TArray<FText>& SomeTextEntries) 
{
    /* some arbitrary code here */
}
```

Be sure to check your returns.
