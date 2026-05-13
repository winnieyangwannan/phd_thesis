# A new kind of species

It is something else. I have started to think of it as a new kind of species, and I want to try to say what I mean.

### The wrong analogies

The first temptation is to map the new system onto the most familiar old one. So we get debates about whether LLMs *really* think, or *really* understand, or *really* feel.  Both sides were defending a category, and the category had been built for a system that had never existed before.

Andrej Karpathy put the alternative in a phrase: *We are not building animals. We are summoning ghosts* [karpathy2025].  Animals come into the world after a billion years of evolution, with most of their hardware already wired. A zebra stands within minutes of being born, runs within hours, and follows its mother by sundown; nobody trained the zebra. The training happened in deep time, encoded somehow into the genome. 

Language models are something else. They begin from imitation. We pour the written residue of a civilization into a system that has no body, no birth, no need to eat, no internal states, no intrinsic motivation, no curiosity. The system learns to continue our sentences. What comes out is fluent in everything we have ever written down and naive about everything we have not. It is in this exact sense that they are ghostly: they are made of us, but they are not us, and they did not arrive by the path that anything alive arrived by.

### Savant kids

Karpathy notes the consequence as a paradox. Today's models can pass doctoral qualifying exams and then fail at things a kindergartner finds easy. He calls them *savant kids*. They have a perfect memory and can convincingly generate content that looks correct. The interesting move, the one I find myself wanting to pass on, is not to count this as a failure to be human. It is a feature of a different kind of thing. *Human intelligence actually benefits from being bad at memorization*, Karpathy points out: forgetting is what forces us to abstract, to find the regularity, to see the forest for the trees. A model that remembers everything has no such pressure. Whatever it ends up doing instead, that is the substrate we are now living with.

I exhibits a "jagged profile" of abilities rather than a smooth, well-rounded intellect. Models can demonstrate superhuman or PhD-level performance in highly complex domains—such as winning a gold medal at the International Mathematical Olympiad or writing sophisticated code—yet simultaneously fail at basic commonsense reasoning


If you ask a frontier model, "There is a car wash 50 meters away—should I walk or drive?", the model will often confidently advise you to walk because it calculates that 50 meters is an incredibly short distance. It entirely misses the basic physical requirement that the car itself must be present to be washed.  

Yet, simultaneously, that exact same model architecture can successfully refactor a 100,000-line codebase or discover zero-day vulnerabilities in production software. Code is verifiable; a compiler acts as a perfect RL reward signal, driving superhuman performance. Common-sense physical logistics have no such automated unit test, leaving a massive gap in reasoning.


### A different tech tree

Michael Nielsen has a thought experiment I find clarifying [nielsen2025]. If we ever met an alien civilization, would they have invented our science? The default assumption, the one I held without noticing, is yes. Science is what you do when you start to think carefully; everyone gets to the same place eventually. Nielsen's point is that this is almost certainly wrong. The tech tree is enormous. The branch we climbed is contingent. We started with bodies, with eyes, with a particular chemistry, with a particular set of mathematical accidents in the seventeenth century. Aliens would start somewhere else and end somewhere else. There is no reason to expect their physics to look like our physics, except in the bits where the universe is forcing both hands. Most of the tech tree, Nielsen says, will never be explored at all.

LLMs are not aliens, but they are the first system I know of that occupies a clearly different branch of the tree from us. They got language before bodies, abstraction before sensorimotor experience, a million-author corpus before any individual life. They are climbing through capabilities in an order no biological lineage has ever climbed in. Some of what they do well is exactly what they should do well given that order: pattern completion across vast text, statistical regularities in argument structure, fluent recombination.

When an animal develops, its capabilities are highly coupled and physically grounded. A biological agent capable of complex navigation also possesses the underlying sensory-motor foundations to understand physical constraints and consolidate memories of how the world works.  LLMs, conversely, are not evolving animals; Karpathy calls them "summoned ghosts." They absorb statistical patterns from a vast ocean of human text without any cohesive, grounded cognitive architecture. They arrive with the specialized knowledge to write a PhD-level analysis on complex systems, while simultaneously possessing the cognitive blind spots of a confused grade-schooler. This lack of an integrated world model—where an agent continuously learns and anchors its behavior to physical realities—is why the capability profile of current systems remains so starkly uncoupled and irregular



### Copernican Revolution

Just as Copernicus had to dislodge the Earth from the center of the solar system, we may now have to dislodge the human mind from the center of the space of intelligences. The error, on Tao's account, is to evaluate AI on a single linear axis that runs from *dumb* through *human-level* to *superhuman*, with us as the calibration point [tao2026]. The axis itself is the mistake. AI is not a smaller or larger version of the kind of mind we have; it is a different kind of mind on a different axis entirely. The work is not to ask whether the new system is above or below us on our scale. The work is to figure out what scale it is on at all.

Terence Tao, working with these systems day to day on real mathematics, has put the same observation in a different vocabulary [tao2026]. *They excel at breadth*, he says, *and humans excel at depth.* The two profiles are complementary, and our current institutions of science are tuned almost entirely to depth, because that is what humans are uniquely capable of. The arrival of a system whose cognitive shape is different in this specific way is not an incremental upgrade. It is a new axis. We will need to redesign how we do science to take advantage of breadth, the same way physics had to be redesigned to take advantage of mathematics it had not previously needed.

The little parable I keep telling myself comes from chess. Magnus Carlsen, the strongest human player of his generation, seems to have quietly retooled his game after the AlphaZero papers came out. AlphaZero was willing to give up a pawn for the promise of a slow strangle fifty moves later, and to play moves that looked simply ugly to a human eye. Carlsen began experimenting with the same kind of long, structural sacrifice. He has said in interviews that he finds the willingness to give up pieces fascinating, and that he is still trying to learn the art. A human grandmaster learned chess from a non-human player. This is what cross-species exchange can look like. It is not yet the gains-from-trade between civilizations that Nielsen imagines, but it is a small premonition of it.


### A closing image

When I look back at the work in this dissertation, I think the through-line was: what does memory look like when the substrate is different? In Part I, the substrate is biological tissue under selection pressure. In Part II, it is a transformer trained on an internet of human text. In Part III, it is a system of agents that can rewrite themselves. Three substrates, three answers, no merger. The point was never that they were the same. The point was that they were different in ways worth looking at.


Karpathy has another line I think about often. *What I cannot build, I do not understand.* And then, more honestly: *what I can build, I still don't understand.* The history of AI in my lifetime has been the history of building things faster than we can interpret them. We have, in a real sense, summoned something. We are now living in the early period of trying to figure out what it is.

I would like to be alive for the part of the story where we figure out what we have on our hands.
