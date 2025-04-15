# CBT905
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 905 is from Sam Golob (initially) and contains common     *   FILE 905
//*           storage information (CSA) about some of the PARMLIB   *   FILE 905
//*           members in z/OS.  This is (of necessity) a work in    *   FILE 905
//*           progress.  We want to add information about more      *   FILE 905
//*           PARMLIB members, as we accumulate more knowledge      *   FILE 905
//*           and contributions from people.                        *   FILE 905
//*                                                                 *   FILE 905
//*           We want to reveal the addresses that show how to      *   FILE 905
//*           access each PARMLIB member's common storage address   *   FILE 905
//*           (CSA) block(s) of information.  We'll do it, one      *   FILE 905
//*           PARMLIB member at a time, and keep adding members     *   FILE 905
//*           as we can.  We invite anyone who knows about any      *   FILE 905
//*           PARMLIB member's CSA information to please update     *   FILE 905
//*           this file with your knowledge, and send the           *   FILE 905
//*           information to me, so I can add it in.  Thanks much.  *   FILE 905
//*                                                                 *   FILE 905
//*           Each member name of this pds will correspond to a     *   FILE 905
//*           PARMLIB member name.                                  *   FILE 905
//*                                                                 *   FILE 905
//*       email:  sbgolob@cbttape.org                               *   FILE 905
//*                                                                 *   FILE 905
//*       Explanation:                                              *   FILE 905
//*                                                                 *   FILE 905
//*           It makes sense that every (or almost every) PARMLIB   *   FILE 905
//*           setting is reflected somewhere as information in      *   FILE 905
//*           common storage.  Otherwise, how could the system      *   FILE 905
//*           use this information or refer to this information?    *   FILE 905
//*           So it is our aim to start with selected PARMLIB       *   FILE 905
//*           members that we know about, and show how and where    *   FILE 905
//*           their PARMLIB settings are reflected in common        *   FILE 905
//*           storage.                                              *   FILE 905
//*                                                                 *   FILE 905
//*           The starting point for our investigation is of        *   FILE 905
//*           course, the z/OS Initialization and Tuning Reference. *   FILE 905
//*                                                                 *   FILE 905
//*           Member names in this pds, will correspond to          *   FILE 905
//*           PARMLIB member names, as described in the Init        *   FILE 905
//*           and Tuning Reference manual.                          *   FILE 905
//*                                                                 *   FILE 905
//*       Further Explanation:                                      *   FILE 905
//*                                                                 *   FILE 905
//*           Obviously, the system, in order to reference the      *   FILE 905
//*           values stored in these common storage areas, needs    *   FILE 905
//*           an "address".  We see that all of these areas are     *   FILE 905
//*           found using one or more definitely defined addresses. *   FILE 905
//*           That being the case, we want to reveal the addresses  *   FILE 905
//*           which show how to access each PARMLIB member's        *   FILE 905
//*           block(s) of information.                              *   FILE 905
//*                                                                 *   FILE 905
//*           Where are the addresses to each area?  Of course      *   FILE 905
//*           they are known to the IBM system developers.  But     *   FILE 905
//*           many of them are known to us too.  IBM macros         *   FILE 905
//*           define all these areas.  Many of the IBM macros       *   FILE 905
//*           are distributed in SYS1.MACLIB, SYS1.MODGEN, or       *   FILE 905
//*           other places.  Others of these macros are internal    *   FILE 905
//*           to IBM only.  IBM developers know about them, but     *   FILE 905
//*           we "outsiders" have to figure them out.  Some of      *   FILE 905
//*           those areas have been "figured out" already, by       *   FILE 905
//*           people who needed to display the information, and     *   FILE 905
//*           we want to publish as much of that info as we can.    *   FILE 905
//*           For the purpose, we have included the SHOWzOS         *   FILE 905
//*           macro library in this pds, as member SHOWMACS.        *   FILE 905
//*           SHOWMACS includes descriptions of many internal       *   FILE 905
//*           IBM macros whose layouts people have figured out.     *   FILE 905
//*                                                                 *   FILE 905
//*           So, it is our aim to help the programmer who wants    *   FILE 905
//*           to find "system internals" information about each     *   FILE 905
//*           PARMLIB member.  Since this is a daunting task,       *   FILE 905
//*           we will start with the few members we know about,     *   FILE 905
//*           and we'll grow the collection from there.  ANYONE     *   FILE 905
//*           and EVERYONE is invited to contribute, in the areas   *   FILE 905
//*           that he/she knows about.  Please help us expand       *   FILE 905
//*           this collection of knowledge.  Thank you, in advance. *   FILE 905
//*                                                                 *   FILE 905
//*       PARMLIB Members Currently Supported:                      *   FILE 905
//*                                                                 *   FILE 905
//*           DEVSUP                                                *   FILE 905
//*           IKJTSO                                                *   FILE 905
//*           LPALST                                                *   FILE 905
//*           VATLST                                                *   FILE 905
//*                                                                 *   FILE 905
```
