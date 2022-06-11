# quest-submissions

# Chapter 1.0 : Day 1 
  1: The Blockchain in my own words  
     A place for people to write and deploy smart contracts
     with shared databases on different nodes on a network.
     People can then use transactions to run these smart contracts.
  
  2: A smart contract is a simple program stored on the blockchain
     that participants involed can rely on smart contracts automateing
     the process and know that they both will be satified with the outcome.
     
  3: A transaction is a glorified paid function call, and a script is
     used to view data on the blockchain and has no cost.<br>
     <i>JT:</i><br>
     <i>...transactions are paid, scripts are free. Transactions change data on the blockchain, scripts simply read data</i>
     
# Chapter 1.0 : Day 2
  
  1: Safety and Security, Clarity, Approachability, Developer Experience, Resource Oriented Programming
  
  2: The five pillars are useful because they keep everything inline and incheck without it there would only 
     be chaos. With all five pillars in place everyone involved can feel at ease when approaching a secure and 
     easy to mangage application.
     
# Chapter 1.5 : Reviewed
  https://www.codecademy.com/<br>
  

# Chapter 2.0 : Day 1
# 1:
![image](https://user-images.githubusercontent.com/12196769/172684905-69efb587-840c-4755-a9e8-fce2b63e088f.png)<br>

# 2:
![image](https://user-images.githubusercontent.com/12196769/172685025-3d659f1d-79e9-466c-aeb2-a0c6193e3922.png)<br>

# Chapter 2.0 : Day 2
  1: Because it doesn't modify the state. We want to change our information.<br>
  2: If we need to access data on an account we can use AuthAccount in the prepare phase which means we are approving this transation.<br>
  3: Difference in Prepare Phase and Execute Phase is Prepare is where we access the information/data in the account and Execute is when we change the data.<br>
  4: <br>
  # Contract:
  ![image](https://user-images.githubusercontent.com/12196769/172897529-acfa5895-47c2-42b4-a619-d140a451c904.png)<br>
  # Transaction:
  ![image](https://user-images.githubusercontent.com/12196769/172896880-63306753-ad67-4ef1-9d8c-d3047546e655.png)<br>
  # Script:
  ![image](https://user-images.githubusercontent.com/12196769/172897086-0a48d577-a2cf-4bfa-b38e-d64ab6f8e491.png)<br>

# Chapter 2.0 : Day 3
  1:<br>
  ![image](https://user-images.githubusercontent.com/12196769/173107977-b0686f4c-292c-45fb-973a-96be27182bc5.png)<br>
  2:<br>
  ![image](https://user-images.githubusercontent.com/12196769/173117786-4b2f0d27-d034-49f1-b8d9-7f8b02643dd7.png)<br>
  3: When accessing values from a Dictionary you will always have optionals. So if you want the actual type and not the otional you must unwrap it.<br>
  Example<br>
  ![image](https://user-images.githubusercontent.com/12196769/173171800-b8345510-0856-4bf8-a214-84bb9b5eb8b5.png)<br>
  <i>On line 3 the ? is not nessary since an optional is returned by default.</i><br>
  4:<br>
  * What the error message means:
    Return Type used was a String, but the Value Returned was an optional.
  * Why we're getting this error
    Type Mismatch Return Value does not match the Return Type
  * How to fix it
    You can change the Return Type to String?<br>
    ![image](https://user-images.githubusercontent.com/12196769/173122834-00978e2f-db34-4450-9e32-9895c03fbc4d.png)<br>
    You could even use a Force-Unwrap Operator<br>
    ![image](https://user-images.githubusercontent.com/12196769/173123025-5e7cfae9-ef3c-461b-8384-48b73b05ef9a.png)<br>
 
 # Chapter 2.0 : Day 4 ***Still working on ***
   1: *Account Code*<br>
   2: *Account Code*<br>
   <details>
   <summary>Accounts Code</summary>
      pub contract Hero {

    pub var allStats: {Address: Stats}

pub struct Stats {
    pub let health: Int
    pub let armor: Int
    pub let potions: Int
    pub let account: Address

    init(_health: Int, _armor: Int, _potions: Int, _account: Address) {
        self.health = _health
        self.armor = _armor
        self.potions = _potions
        self.account = _account
    }
}
pub fun addStat(health: Int, armor: Int, potions: Int, account: Address) {
        let newStat = Stats(_health: health, _armor: armor, _potions: potions, _account: account)
        self.allStats[account] = newStat
    }

    init() {
        self.allStats = {}
    }

}
   </details>   
  [image](https://user-images.githubusercontent.com/12196769/173178983-762f3372-2be6-4669-8942-d224579d61bf.png)<br>
  3:<br>
  <details>
  <summary>Account Code</summary>
  import Hero from 0x01

transaction(health: Int, armor: Int, potions: Int, account: Address) {

    prepare(signer: AuthAccount) {}

    execute {
    Hero.addStat(health: health, armor: armor, potions: potions, account: account)
        log("We're done.")
    }
}
  </details>
  ![image](https://user-images.githubusercontent.com/12196769/173179402-7ee9e929-c57f-4dab-be4e-a3dfaacb591f.png)<br>
  4:<br>
  
