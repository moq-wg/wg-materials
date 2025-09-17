
# Wednesday

## 0930-0945 Administrivia

## 0945-1015 Victor - Object Status
* PR #1118 More explicit handling for end-of-group bit
* #1093 End of Group flag in Subgroup/Datagram Header creates new ways to malform a track
* #1223 Do we ever need to explicitly send "Object Does Not Exist" on the wire?
* #1224 Do we need Object Status and Prior Group/Object ID extensions in FETCH replies?

## 1015-1045 New Group Signaling (Mike)
* #1028 Allowing subscribers to trigger a new sync point (new group) in a track
* PR #1060 DYNAMIC_GROUPS and NEW_GROUP_REQUEST parameters
* PR #1219 Dynamically generating new Groups

## 1045-1100 Break

## 1100-1130 Implementation Experience (Luke)

## 1130-1230 Lunch with Demos (Ali/Zafer)

## 1230-1445 MoQT Issues (Alan):

### [15] Immutable header extensions
* Already resolved, propose move expiration here since it impacts #1012

### [15] Finalize Parameter vs Field Decisions
* #872 What if the subscriber needs an immediate SUBSCRIBE_UPDATE?
* #878 Make SUBSCRIBE group order into an optional parameter
* #879 Make SUBSCRIBE filters into optional parameters
* PR #1210 Parameters for Group Order, Subscribe Priority and Subscription Filter
* PR #1012 Make expires a parameter
* PR #1052 Make Largest Location a Param

### [45] Subscribe and Fetch filtering
*	#441 Ability to filter which Objects are sent in a Subscription
* #1068 Outside-in compression: scaling MOQT for high capacity ingest
* PR #1164 RFC: Generic Filters for Subscriptions and FETCH

### [60] Subscribe Namespace Track filtering/selection (Mo/Suhas)
*	#1206 Filter / select across multiple tracks in a namespace

## 1445-1500 break

## 1500-1700 More MoQT Issues (Alan)

### [30] Extensibility Model and Grease
* #416 Extensibility and greasing
* #1175 Handling of non-defined error codes

### [20] Expiration
* #1026 Proposed new requirements for expires

### [30] Subscribe Update acknowledgements and Publish Update
* #1003 No way to know if/how a SUBSCRIBE_UPDATE was processed
* #1182 Proposal for REQUEST_OK message

### [40] General issues, esp. wire format

**Wire Format**

* #660/PR #949 FETCH serialization
* #549/PR#1016 Varints
* #1204 FETCH priority update
* #781/PR #1176 Track Extensions
* #794 Object Extension Types should not rob the bottom bit for even/odd games
* #1184 Determine if/where we should use TV instead of TLV
* #1221 Requiring known Parameters to be understood and optimizing the framing
* #1162 Should we remove INTERNAL_ERROR?
* #1158 Cacheability of MALFORMED_TRACK
* #1168 Ephemeral vs Long-lived Request IDs
* #1183/PR #1220	Subscribing to all publishers for a Track's namespace can be wasteful	

**Frame Headers**

* #915 Swap Type and Size in control messages?
* #1212 Skip the Length field for some types of control messages?

**Auth Block**

* #996 On repetition of the AUTHORIZATION TOKEN parameter
* #969 Do we really need Authorization Alias ?
* #944 Reuse of Authz Alias Parameter
* #1078 Disallow USE_ALIAS and DELETE auth token ops in CLIENT_SETUP

# Thursday

## 0930-0940 Administrivia

## 0940-1000 Interop Report (Mike)

## 1000-1015 Next Interim Planning / Meet in Shenzhen? (Martin)

## 1015-1030 Break

## 1030-1130 WARP, etc (Will)
- WARP (25min) https://github.com/moq-wg/warp-streaming-format
- CAT-4-MOQT (20min) https://github.com/moq-wg/CAT-4-MOQT
- CARP (10min) https://github.com/wilaw/carp

## 1130-1150 LOC (Mo)

## 1150-1250 Lunch

## 1250-1430 General MoQT Issues (Alan)

* Continue from Wednesday List, plus

## 1430-1445 Break

## 1445-1600 0RTT, Datagrams (Ian)



# Other Issues To Discuss, As Time Permits

### Other Needs Discussion:

* 668 Should sending GOAWAY also block SUBSCRIBE, etc.?
* 1124	What are the rules for overlapping prefixes in UNSUBSCRIBE_NAMESPACE?	
* 1070 Is it a protocol error to get ANNOUNCE_CANCEL before ANNOUNCE_OK/ANNOUNCE_ERROR?	
* 869 Difficult to limit resource consumption of a Subscription	
* 836	Elaborate on the role of the original publisher	

#### We keep talking without progress, low pri?

* 1036	Should we get rid of FETCH_ERROR + No Objects?	
* 764	Should we merge Track Namespace and Track Name?	
* 746	Way for FETCH error to say range was too large		


#### Delivery Timeout (no discussion planned)

* 667 DELIVERY_TIMEOUT is unimplementable	
* 606	Delivery timeout cannot be expressed per subgroup	

#### ABR (no disucssion planned)

* 534	Allow padding streams	
* 471	Should any priority values indicate "Less than best effort"? / How do you upswitch without causing user harm?	


### Other Needs PR that (probably?) just need a PR

* 1160	MoQ over raw QUIC default port
* 1144	Is TRACK_STATUS_OK with track_alias > 0 an error?
* 1121	Parameters are only one per Message by default, Objects are unstated
* 1041	Namespace/Name Edge cases
* 770	Allow widening a subscription in SUBSCRIBE_UPDATE
* 748	Extension (and parameter) ordering


### Other Untriaged (TBD, will udpate)

* 1177	Need a way to pause/resume a track in the data plane	
* 1174	Provide guidance on text encoding	
* 1103	Delivery timeout, Datagrams, and Caching	
* 1101	Track switching at the live edge using MOQT's current messages?	
* 1064	TRACK_STATUS[_OK] has useless fields	
* 1057	Is knowing no Objects in a Fetch are Unknown practical?	
* 1040	Flow control with SVC	
* 1039	Simplifying joining at the latest available join point.	
* 1023	Subgroups and DELIVERY_TIMEOUT can result in pathological FETCH	
* 945	FETCH stream stalls if Objects exist and will be published, but are lower priority	
* 861	Are Groups really join points anymore / SUBSCRIBE start on group boundaries	
* 843	ANNOUNCE via SUBSCRIBE_ANNOUNCES vs ANNOUNCE by itself	
* 799	How can end subscriber verify an authorization claim in an ANNOUNCE	
* 786	Are UNANNOUNCE different purposes clear to subscriber	
* 783	Missing aspects in the security consideration section	
* 380	MoQ and power consumption	
