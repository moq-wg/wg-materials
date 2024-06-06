# Use cases for MoQ Priority

A primary use of Priorities in MoQ will for an application to signal to a relay what to send next to a subscriber 
when there is more than one thing to send.  Other uses might include alocating other resources (eg: publisher encoding CPU),
or for setting fields in lower level protocols.

Some other tools besides a priority signal can also be used to meet some use cases (eg: unsubscribe, cancellation, flow control, request pattern).

## Use Case 1: Prioritize one track relative to another track

### Examples

* Audio tracks over video tracks
* Resolution A over Resolution B (multiple qualities)
* Base layer track over enhancement track
* Input movement tracks over media tracks
* Dominant speaker video track over non-speaker video tracks
* Pinning a participant video to a large window
* Visible tabs in a browser over those without focus

**Question**: Do we envision applications where a single subscriber requests tracks through the same relay from
multiple uncoordinated publishers?

## Use Case 2: Prioritize groups/objects in a track relative to other groups/objects in the same track

* New groups/objects over older groups/objects - prefers freshness<br>
_Example_: Live or interactive media

* Older groups/objects over newer groups/objects - prefers fidelity<br>
_Example_: Live rewind / VoD

* Object that needs to be decoded/played next 

## Use Case 3: Bandwidth sharing - alternate between tracks, with weights

* Prefer playing tracks over prefetch tracks without starvation<br>
_Example_: fast channel switching, short form video apps.<br><br>
 In these use cases, the playing video may not be explicitly selected by a viewer, 
 cannot assume it should be exclusively prioritized over prefetch.

## Use Case 4: Synchronization and ordering - sending objects from different tracks at sensible times

* Prevent _later_ audio track from blocking _earlier_ video track
* Prevent _later_ prefetch track A from blocking _earlier_ prefetch track B<br>
_Example_: Watching 1 video while prefetching 3 others
