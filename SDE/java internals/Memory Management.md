Garbage collection in java:

2 levels of garbage collection:
young generation :
include the eden generation which are just created objects and the surviving generation which includes objects which have survied some of the minor gc events.

these are stored in the ram where we make use of the spacial continuity as remember that the objects created are sequencially places so a sequencial scan can be used to quickly do garbage collection.

old generation these reside in the ram(heap) but as there is physical distance when it comes to the physical address, we maintain a page mapping where the virtual address is mapped to physical address and this page is cached in the cpu the point being that the old generation has already survived multiple gc cycles and will probably will be used again.


what triggers gc cycles:
minor gc:
when the space for storing eden objects or surviing objects are full
takes few ms no major impact.
or objects move out of scope

major gc:
requirs scanning of entire heap so takes a lot of time hundreds of ms and even seconds ,very expensive, happens when no space left for allocation of periodic gc cleanup happens.