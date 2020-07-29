# Actors
Actor is one of the most important aspects of Unreal Engine, it lays at the core of everything you will do interacting in the Unreal Editor viewport and the Game World. This core Unreal Engine Class {{code|AActor}} forms the basis for any Object you can see in the viewport in the 3d space, this does not include UMG widgets which are overlays.

### Components
Actors are composed of various [Components](Components.md)

### Info

## Spawning
Spawning refers to the process of creating an Actor, similar to New Object though having a physical presence in the game world means Actors are treated differently, because they have components like collision. If an Actors Spawn location is being blocked we call that Encroachment, its when two Actors (or more) share the same physical space.

### Owner
Part of the Actor framework within Unreal Engine is the ability to get the Owner of an Actor, this is the Actor which either initiated the Spawn call or you can specify an Owner within the Spawn function. Getting the Owner is done through the {{code|GetOwner}} function defined in {{code|AActor}}.

### Instigator
Sometimes you need to get the Actor which actually initiated a Spawn which can be different to the Actors Owner, this is where Instigator comes in. For example a Weapon might be the Owner of a Projectile but the Instigator is the Character which fired the Weapon, so when you {{code|GetInstigator}} on a Projectile it would return the Character.

## Destroying
If you are finished with an Actor simply call the {{code|Destroy}} method.

## Archetypes

## Attachment

### Detachment

### Sockets

### Editor

## Replication

### Actor Channels

## Further Reading
[https://docs.unrealengine.com/en-US/Programming/UnrealArchitecture/Actors/index.html Actors Architecture]

### C++
{{epic|https://docs.unrealengine.com/en-US/API/Runtime/Engine/GameFramework/AActor/index.html Actor API}}

### BP
{{epic|https://docs.unrealengine.com/en-US/Engine/Actors/index.html Using Actors in Unreal Editor}}
{{epic|https://docs.unrealengine.com/en-US/Engine/Blueprints/BP_HowTo/ActorReference/index.html Actor References in Blueprint}}
{{epic|https://docs.unrealengine.com/en-US/BlueprintAPI/Actor/index.html Actor}}

Back to [Main Page](../README.md)