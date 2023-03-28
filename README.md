# Simple_DAO
 

# DAO :- Decentralized Autonomus Organization.

-->There is very less human intervention in DAO. Trust is build due to Smart contracts and decentralized behaviour of DAO.

-->DAO is a digital organization or corporation run by specific set of rules encoded as computer programs on the blockchain, rather than by traditional management structures.

-->The rules and transactions are made by a decentralized network of computers, making it resistant to censorship, fraud, and control by single entity.

-->Members of DAO use blockchain based tokens to vote on proposals and make decisions collectively.


# DAO Functions

-->constructor(uint _contributionTimeEnd, uint _voteTime, uint _quorum)

   ---->"_contributionTimeEnd" refers to the time limit which is set for the investors for contributing to the project.
   
   ---->"_voteTime" refers to the time limit set for voting for proposal.
   
   ---->"_quoram" refers to the minimum number of people required to pass a proposal.
   
   
-->function contribution() external payable
 
 ----> This function allows investors to contribute to the project by buying tokens. This "payable" keyword allows contract account to receive ethers or any other crypto or tokens.
 

--> function transferShare(uint amount, address to) public onlyInvestor()

----> This transferShare function allows investors to transfers tokens to other accounts. It has modifier onlyInvestor() which restrict the function such that it can only be called by investors or what ever is specified in onlyInvestor() modifier.


-->function redeemShare(uint amount) external onlyInvestor()

----> This functin allows investors to redeem their tokens.


--> function voteProposal(uint proposalId) public onlyInvestor()

----> This function is used to vote for the proposal.


-->function createProposal(string calldata description, uint amount, address payable recipient) onlyManager

---->This createProposal function is used to create proposal, It has three arguments "description" describes the details about the proposal, "amount" it is used to tell how much amount of investment is needed, "recipient" is used to tell whom to send the ethers.


-->function executeProposal(uint proposalId) public onlyManager()

----> This function is used for executing the proposal which will only be called by manager.


--> function allow(address to) public onlyManager() .......function disallow(address to) public onlyManager()

---->These functions are used to allow and restrict some user addresses.


-->function ProposalList() public view returns(proposals[] memory)

----> this function will return the list of all proposals available.




