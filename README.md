# Voting Project

This project allows a basic voting process. It comes with a voting smart contract, units tests for that contract, and files to deploy that contract.

The test coverage is 100%. The tests perimeter is concentrated around the voting contract. Ownable by Open Zeppelin is considered as secured, even if the onlyOwner modifier is tested for some functions.

The tests are organised along the workflow of voting : registration of voters, proposals session, voting session and vote count.

For each step, the beforeEach function build an example a voting session at the considered step, and tests then cover all cases that may occur in this session path,
with three general categories : process itself (proposals, votes...), conditions of processing (requirements, modifiers...) and the workflow status that allows following the whole process.
With in each category a systematic approach in two parts : what is supposed to be possible at this step, and what must be impossible at this step.

According to the long enum WorkflowStatus, many tests can seem the same, but are realized in different times of the process. It was obligatory to get 100% coverage, especially regarding the "branch" column of Hardhat coverage command. But this way the contract is fully covered.

This time approach, step by step, of the tests was thought to ensure covering the whole contract, but also to be more easily understandable to anyone coming up to see. 

Some ameliorations could have been apported to the global process, using new requirements for example, especially to check the proposals entered by users (not two same proposals, clear proposals...) and the related tests. But with the given original contract, job seems to be done.

To be continued... 
