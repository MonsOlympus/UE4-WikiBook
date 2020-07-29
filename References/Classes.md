# Classes
Unreal Engine 4 is based around several [https://en.wikipedia.org/wiki/Programming_paradigm paradigms], one at the core is [[Object Orientation]]. This describes Classes and Objects as basic building blocks, especially in relation to the C++ and C# programming languages which the Unreal Engine is built ontop of as its foundation.

### Inheritance
In [https://en.wikipedia.org/wiki/Class-based_programming Class Based Programming] (a style of OOP) inheritance occurs through defining classes of the objects you intend to use. 

#### Example One
As a basic example {{code|YourObject}} is declared as a child of {{code|Object}}.

*Object
**YourObject

{{code|YourObject}} derives its functionality from its parent. Lets say Object has the function (method) {{code|GetClass()}} your Object will also have this function since its implemented in its parent.

*Object::GetClass()
**''YourObject::GetClass()''

#### Example Two
A more complex example might be two classes extending different Objects.

*Object
**''YourObjectA''
**ActorComponent::DestroyComponent()
***''YourObjectB::DestroyComponent()''

In the above only ''your Object B'' can call the {{code|DestroyComponent}} method since that function is implemented in the {{code|ActorComponent}} the '''child''' of {{code|Object}}.<br>
Where ''your Object A'' does not have the {{code|DestroyComponent}} method, it only has the methods defined in its '''parent''' {{code|Object}}.<br>
It is also important to note that since {{code|ActorComponent}} is a '''child''' of {{code|Object}} it (along with ''your Object B'') inherits all methods from the parent but none from ''your Object A'' because it's not a '''direct descendant''' in the Class Hierarchy (or Tree).<br>

{{tip|It's not just methods which are inherited but all members of that class.}}

### Property System
An object can be a variable, a data structure, a function, or a method, which is why all types in the [[Unreal Property System|Property System]] start with the U prefix.
{{warning|set to change in UE4.25}}

### Blueprint
[Blueprint] is used to create classes from within Unreal Editor, these are Asset Types as well as referring to the Graph Editor itself.

## Defining Classes
As you can see from the below, all Objects defined {{code|UCLASS()}} require the {{code|GENERATED_BODY()}} macro so that property system can properly manage them.
{{warning|Unreal Engine versions earlier than version 4.11 {{code|GENERATED_UCLASS_BODY()}} was used instead.}}

# Objects

## Garbage Collection


## Polymorphism

## Object Literal
{{epic|https://docs.unrealengine.com/en-US/API/Runtime/CoreUObject/UObject/FindObject/index.html Find Object}} 
{{epic|https://docs.unrealengine.com/en-US/Programming/Assets/ReferencingAssets/index.html Referencing Assets}}

## Further Reading
{{epic|https://docs.unrealengine.com/en-US/Gameplay/ClassCreation/index.html Class Creation}}
{{epic|https://docs.unrealengine.com/en-US/Programming/UnrealArchitecture/Reference/Classes/index.html Gameplay Classes}}
{{epic|https://docs.unrealengine.com/en-US/Programming/UnrealArchitecture/Objects/index.html Objects}}
{{epic|https://docs.unrealengine.com/en-US/Programming/UnrealArchitecture/Objects/Optimizations/index.html Unreal Object Handling}}

### Wikipedia
[https://en.wikipedia.org/wiki/Class_(computer_programming)]
[https://simple.wikipedia.org/wiki/Class_(programming)]
[https://en.wikipedia.org/wiki/Object_(computer_science)]

### Others
[https://www.w3schools.com/cpp/cpp_classes.asp]

Back to [Main Page](../README.md)