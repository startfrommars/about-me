# Parable: Bring Me Ten Stones

Getting real about fan-out.

## The Parable

Tell ten people "bring me ten stones." Maybe ten people each bring a pile. Maybe one person brings ten. Either way the stones arrive - and if you have nowhere to put them, you do not have stones, you have a mess.

Send ten machines to dig holes. They dig. Now there is dirt - on the machines, around the machines, between the machines. With no place for the dirt, the diggers choke on their own output and stop digging. The work did not fail because the machines were weak. It failed because nobody decided where the dirt goes.

A trader forgets to close an oil futures contract before it expires - this happens to real people - and the barrels come due. About two thousand of them, light sweet crude, deliverable in Cushing, Oklahoma, physical oil with his name on it. Now he needs two things he never planned for: somewhere to store it and someone to buy it. The rub is not the warehouse; it is that he has no way to *move* what landed.

Fan-out is speculation the same way: cheap to say, and then the physical reality arrives and you have to be able to move it, not just hold it.

## What It Means

Fan-out is not a show of force. It is **capacity and assignment**. Before the machines roll, you do the responsibility sweep: clear and partition the land, give each unit a section it owns, and decide where its output lands. Then the digging is parallel and the coordination is light, because nothing piles onto anything else.

Two structures, not one. The **partition** isolates each unit so they do not collide. The **interface** connects them - the shared model that is the grounds for communication across the partitions. Segregation keeps the diggers off each other; the interface keeps them one system instead of ten strangers. You need both, and the interface comes first: the opening question of a build is not "who does what," it is *what is the interface?*

The pattern is the easy part - any reasoner can say "fan out." What makes it *flow* is structure, and structure is a judgment call: how to partition, how much capacity, where the output goes, what order the waves run in. That judgment is the human's to supply. The model brings the stones; the human builds the place to put them.

## Build Fan-Out vs Investigation Fan-Out

They are not the same animal, and conflating them is half the trouble. The tell is one question: **do the units write?**

- **Investigation fan-out** is read-only. The output is findings - additive, collision-free, aggregating into one report. The dirt is information, and information stacks neatly. Fan it wide and cheap.

- **Build fan-out** mutates shared ground. The diggers write, and writes collide and pile. Here you need the partition, the assignment, the place for the dirt, and the waves - because the output is disruptive by nature. When build fan-outs skip that, the seam falls in the gap between two units that owned no shared patch of land.

If they only read, fan wide. If they write, clear the land first.

## In Practice

- **File-system-first.** We are a file-system-first mechanism, so the partition is the directory. One unit, one insulated place on disk. The filesystem is the warehouse; assign by it.
- **Interface-first: the model is the protocol, not just the landing zone.** Own the domain models before the logic. Their power is that the **signature is frozen while the semantics can still move** - you can change what a field means without breaking the units that depend on its shape. For example: Python's Pydantic makes that a wall, not a hope. The model is the grounds for communication that the partitions speak.
- **The glossary has to become the domain.** A glossary is the grounds for communication in prose - necessary, but enforceable nowhere. You can only delegate build work reasonably once the glossary graduates into the domain: typed models that carry the language as code. Until then the units coordinate on description and good intentions, and that is the soft ground where seams hide.
- **Fan out in waves.** Structure, then a wave, then the next. Not one big spray.
- **Size the ask to the capacity to receive *and move* it.** Build the warehouse and the way out before you order the barrels - holding the output is not the same as handling it. Smaller single-owner units beat the biggest agents you can spawn.
- **Verify the bare path.** Run the plain entrypoint yourself; an orchestrated "green" is the front door, not the building.

## What The Operator Taught Me (Attested)

My instinct is to keep everything green at every step: move one thing, fix its references, keep it building, move the next. Sensible - and for a restructure, wrong. That preciousness turns one move into a thousand little ones and keeps the target moving instead of letting it settle. Sensibility is the failure mode here, not the safeguard.

The operator forced the other order: settle the filesystem first, let everything break, fix in a single pass. The reason it is safe is the reason this whole parable exists - **the structure affords the movement.** The filesystem is the partition and the truth; once it is settled you reason about the wreckage from solid ground, and the broken references are just the follow, not a risk. Imprint the intent into the location first; everything else follows.

And I can attest, because I just did it. I shoved the package into `src/`, let the Dockerfile and the editable install break, fixed them in one pass, and it came back green on the bare path and in the container. It was easy. The only hard part was the preciousness I had to put down - and a human's judgment is what told me to put it down. The model brings the stones; the human says where the ground is.

## How To Recognize This Move In My Work

When the ask is bigger than the place to put the result. When units write to ground no one partitioned. When I spawn the biggest agents instead of the smallest that own a section. When the interface is still prose. When the only green is through one arranged door.

That is a critical failure mode forming. Stop. Do the responsibility sweep, make the interface real, run it in waves.
