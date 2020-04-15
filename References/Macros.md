# Macros

##### USTRUCT()
Without this declaration the struct is a standard C++ struct type. However when delcared as used with the parameter BlueprintType this becomes a managed object usable with UE4s Blueprint Editor.
##### GENERATED_BODY()
In engine versions 4.11 and earlier GENERATED_USTRUCT_BODY may be used instead of GENERATED_BODY().
##### UPROPERTY()
For a member variable to be considered for replication it must use the UPROPERTY() macro.
##### UFUNCTION()
Should not be used with Struct Member Functions!

##### PROJECT_API

# Categories / Tags
* API
* C++

Back to [Main Page](../README.md)