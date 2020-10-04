# Tips  UnrealCPP

## Get the Player 

AMaClassePlayer m_Player = Cast<AMaClassePlayer>(UGameplayStatics::GetPlayerCharacter(GetWorld(), 0));


## Debug.Log()
text : GEngine->AddOnScreenDebugMessage(-1, 10, FColor::Green, "Hey");

Vector : GEngine->AddOnScreenDebugMessage(-1, 10, FColor::Green, FString::Printf(TEXT("Vector : %s"), *GetActorLocation().ToString()));

console : UE_LOG(LogTemp, Warning, TEXT("Hey"));

## Virtual Method
virtual void MyFunction();  **Override in cpp**


## Test type of attribute
MyclassINeed pouet = Cast<MyclassINeed>(Attribut);
If(pouet != nullptr) => OK

## Distance of 2 point

FVector::PointsAreNear(Vector1, Vector2, distance);

## Call Variable in Blueprint

UPROPERTY(BlueprintReadWrite)



## Call Function in Blueprint

UFUNCTION(BlueprintCallable)


## Edit Function in Blueprint

UFUNCTION(BlueprintNativeEvent)


## For each

for (Myclass* neighbor : TArray<Myclass*> tabMyclass)

## new (Myclass)

NewObject<Myclass>();


## Spawn precise actor

AMyClass * project = (AMyClass *) GetWorld()->SpawnActor<AProjectile>(GetClass(),position, rotation);


## Spawn Actor Template:

TSubclassOf<class AActor>  toSpawn;
GetWorld()->SpawnActor<AActor>(toSpawn, GetActorLocation(), GetActorRotation());

