# Macros

### Definitions
By defining a member as a U macro you are telling Unreal Build Tool you want the Unreal Engine VM to manage it. This gains you advantages like automatic reflection and garbage collection among others.
#### UENUM()
Do not require a GENERATED_BODY().
#### UCLASS()
#### USTRUCT()
Without this declaration the struct is a standard C++ struct type. However when delcared as used with the parameter BlueprintType this becomes a managed object usable with UE4s Blueprint Editor.

#### UINTERFACE()

UE_DEPRECATED(4.23, "Replace with GetAuthoredNameForField or UField::GetAuthoredName")

#### GENERATED_BODY()
In engine versions 4.12 and newer
GENERATED_BODY()

In engine versions 4.11 and earlier
GENERATED_USTRUCT_BODY()
GENERATED_UCLASS_BODY()

#### UPROPERTY()
For a member variable to be considered for replication it must use the UPROPERTY() macro.

In engine versions 4.25 and newer
This will be known as FPROPERTY() as engine API changes were made.

In engine versions 4.24 and earlier
UPROPERTY() is used.

#### UFUNCTION()
Should not be used with Struct Member Functions!

UFUNCTION(BlueprintPure, Category = "Attrbiutes")

#### PROJECT_API

### Logging Macros

#### Headers (*.h)
DECLARE_LOG_CATEGORY_EXTERN(Attributes, VeryVerbose, All);

#### Source (*.cpp)
DEFINE_LOG_CATEGORY(Attributes);
UE_LOG(Attributes, VeryVerbose, TEXT("New Attribute Registered: %s"), *AttributeName.ToString());

#### Other
UE_CLOG( !EnumClass, LogClass, Fatal, TEXT("Couldn't find enum '%s'"), EnumPath );

DECLARE_CYCLE_STAT(TEXT("AbilitySystemComp ApplyGameplayEffectSpecToTarget"), STAT_AbilitySystemComp_ApplyGameplayEffectSpecToTarget, STATGROUP_AbilitySystem);

\#if WITH_SERVER_CODE
	SCOPE_CYCLE_COUNTER(STAT_AbilitySystemComp_ApplyGameplayEffectSpecToSelf);

\#define LOCTEXT_NAMESPACE "AbilitySystemComponent"

			// Log results of applied GE spec
			if (UE_LOG_ACTIVE(VLogAbilitySystem, Log))
			{

## Delegates

DECLARE_DYNAMIC_MULTICAST_DELEGATE(FAttributeTriggerDelegate);

## Editor & Builds

\#if WITH_EDITOR
\#if HACK_HEADER_GENERATOR
\#if ENABLE_GC_OBJECT_CHECKS
\#if WITH_HOT_RELOAD
\#if !(UE_BUILD_TEST || UE_BUILD_SHIPPING)

## Others

check()

FORCEINLINE

DECLARE_CASTED_CLASS_INTRINSIC(UStruct, UField, CLASS_MatchedSerializers, TEXT("/Script/CoreUObject"), CASTCLASS_UStruct)
DECLARE_CASTED_CLASS_INTRINSIC_NO_CTOR(UScriptStruct, UStruct, CLASS_MatchedSerializers, TEXT("/Script/CoreUObject"), CASTCLASS_UScriptStruct, COREUOBJECT_API)
	
DECLARE_CASTED_CLASS_INTRINSIC(UFunction, UStruct, 0, TEXT("/Script/CoreUObject"), CASTCLASS_UFunction)
DECLARE_WITHIN(UClass)

DECLARE_CASTED_CLASS_INTRINSIC_NO_CTOR(UClass, UStruct, 0, TEXT("/Script/CoreUObject"), CASTCLASS_UClass, NO_API)
DECLARE_WITHIN_UPACKAGE()

\#if USTRUCT_FAST_ISCHILDOF_IMPL == USTRUCT_ISCHILDOF_STRUCTARRAY
\#if USTRUCT_FAST_ISCHILDOF_COMPARE_WITH_OUTERWALK || USTRUCT_FAST_ISCHILDOF_IMPL == USTRUCT_ISCHILDOF_OUTERWALK
\#if PLATFORM_COMPILER_HAS_IF_CONSTEXPR

ENUM_CLASS_FLAGS(EGetByNameFlags)

# Categories / Tags
* API
* C++

Back to [Main Page](../README.md)