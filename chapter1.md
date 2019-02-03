# Reduced event data structure

The data used in the framework is organized in an event structure with:
* global event information (_e.g._ vertex position, centrality, triggers, event plane)
* detector related information (_e.g._ V0, T0, FMD)
* list of tracks
* list of pair candidates (V0 candidates: conversions, K0s, Lambda; pair candidates)
* list of calo clusters (EMCAL, PHOS)

The C++ classes containing the data structures are described in the following.

## AliReducedBaseEvent

Base class containing basic event structure. 

**Data members**

1. _Simple type members:_
[import:'DATA'](/home/iarsene/alice-soft/AliPhysics/PWGDQ/reducedTree/AliReducedBaseEvent.h)

2. _TClonesArray lists of tracks:_
[import:'TRACKS1'](/home/iarsene/alice-soft/AliPhysics/PWGDQ/reducedTree/AliReducedBaseEvent.h)
[import:'TRACKS2'](/home/iarsene/alice-soft/AliPhysics/PWGDQ/reducedTree/AliReducedBaseEvent.h)
The two lists are necessary to allow writing in the event both base tracks (AliReducedBaseTrack) and full tracks (AliReducedTrackInfo).

3. _List of pair candidates:_ 
[import:'CANDIDATES'](/home/iarsene/alice-soft/AliPhysics/PWGDQ/reducedTree/AliReducedBaseEvent.h)
Contains V0 candidates (conversions, K0s, Lambda) and pair candidates written as AlireducedPairInfo objects

## AliReducedEventInfo

**Data members**

1. _Simple type members:_
[import:'DATA'](/home/iarsene/alice-soft/AliPhysics/PWGDQ/reducedTree/AliReducedEventInfo.h)

2. _Calorimeter cluster list:_
[import:'CALO'](/home/iarsene/alice-soft/AliPhysics/PWGDQ/reducedTree/AliReducedEventInfo.h)
Contains the list of calorimeter clusters written as AliReducedCaloClusterInfo objects

3. _FMD channel multiplicities_ 
[import:'FMD'](/home/iarsene/alice-soft/AliPhysics/PWGDQ/reducedTree/AliReducedEventInfo.h)
Contains the list of FMD channel multiplicities written as AliReducedFMDInfo objects

3. _Event plane_ 
[import:'EVENT_PLANE'](/home/iarsene/alice-soft/AliPhysics/PWGDQ/reducedTree/AliReducedEventInfo.h)
