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
 
 # Chapter 2.0 : Day 4
   1: Deploy a new contract that has a Struct of your choosing inside of it (must be different than Profile).
   ![image](https://user-images.githubusercontent.com/12196769/173182746-5512b8f6-b3fc-4dd7-802e-20f4d1e9b124.png)<br>
   2: Create a dictionary or array that contains the Struct you defined.     
   3: Create a function to add to that array/dictionary.
   ![image](https://user-images.githubusercontent.com/12196769/173182766-d08ff9a9-852d-4cc0-b938-4f2fbc4b725f.png)<br>
   4: Add a transaction to call that function in step 3.
   5: Add a script to read the Struct you defined.
   ![image](https://user-images.githubusercontent.com/12196769/173182803-ea63963d-cb24-4399-a9a8-80850174beba.png)<br>
   # Accounts
   ![image](https://user-images.githubusercontent.com/12196769/173180956-661c267b-c77a-49cc-9213-2d9665331211.png)<br>
   # Transactions
   ![image](https://user-images.githubusercontent.com/12196769/173181031-1445a99d-68c0-4bf3-81dc-51f3d7627565.png)<br>
   # Scripts
   ![image](https://user-images.githubusercontent.com/12196769/173182685-a1333ca0-29ea-4ffb-854c-a3b3be5a12ae.png)

# Chapter 3 : Day 1
1: <i>In words, list 3 reasons why structs are different from resources.</i><br>
You can create, copy, or overwrite them when ever you want.<br>

2: <i>Describe a situation where a resource might be better to use than a struct.</i><br>
If you were going to do anything with a NFT I would use a resource, since it is harder to lose the information

3: <i>What is the keyword to make a new resource?</i><br>
create

4: <i>Can a resource be created in a script or transaction (assuming there isn't a public function to create one)?</i><br>
No, the create keyword can only be used inside a contract<br>

5: <i>What is the type of the resource below?</i><br>
<pre>
  <code>
pub resource Jacob {

}
  </code>
 </pre>
 Resource type is empty it hasn't been stated yet<br>
 
6: <i>Let's play the "I Spy" game from when we were kids. I Spy 4 things wrong with this code. Please fix them.</i><br>

<pre>
  <code>
pub contract Test {

    // Hint: There's nothing wrong here ;)
    pub resource Jacob {
        pub let rocks: Bool
        init() {
            self.rocks = true
        }
    }

    pub fun createJacob(): Jacob { // there is 1 here
        let myJacob = Jacob() // there are 2 here
        return myJacob // there is 1 here
    }
}
  </code>
</pre>

<pre>
  <code>
  pub contract Test {

    // Hint: There's nothing wrong here ;)
    pub resource Jacob {
        pub let rocks: Bool
        init() {
            self.rocks = true
        }
    }

    pub fun createJacob(): @Jacob { // Was missing the @ symbol to state this is a resource
        let myJacob <- create Jacob() // Using resources we use the <- move symbol followed by create to initizlize myJacob 
        return <- myJacob // again we need to be moving our resource with <- move symbol
    }
}
  </code>
</pre>
# Chapter 3 : Day 2
<pre>
<code>
pub contract Meta {
    
    pub var arrayOfNumbers: @[numbers]
    pub var dictionaryOfImages: @{String: imageName}

    //
    pub resource numbers {
        pub let message: String
        init() {
            self.message = "Numbers_Holder"
        }
    }

    //
    pub resource imageName {
        pub let message: String
        init(){
            self.message = "Image_Holder"
            }
    }
    
    // Array Functions
    pub fun addNumber(number: @numbers) {
        self.arrayOfNumbers.append(<- number)
    }

    pub fun removeNumber(index: Int): @numbers {
        return <- self.arrayOfNumbers.remove(at: index)
    }

    // dictionary functions
    pub fun addImage(image: @imageName){
        let key = image.message
        self.dictionaryOfImages[key] <-! image
    }

    pub fun removeImage(key: String): @imageName {
        let image <- self.dictionaryOfImages.remove(key: key) ?? panic("Could not find the image!")
        return <- image
    }

    init() {
        self.arrayOfNumbers <- []
        self.dictionaryOfImages <- {}
    }

}
</code>
</pre>
# Chapter 3 : Day 3
1:<br>
*Contract*<br>
<pre></code>
pub contract Metadata {
    
    pub var dictionaryOfMeta: @{Int: Meta}

    //
    pub resource Meta {
        pub let id: Int
        pub let name: String

        init(_id: Int, _name: String){
            self.id = _id
            self.name = _name
            }
    }

    pub fun getReferenc(id: Int): &Meta {
        return (&self.dictionaryOfMeta[id] as &Meta?)!
    }

    pub fun depositMeta(Meta: @Meta) {
        self.dictionaryOfMeta[Meta.id] <-! Meta
    }

    pub fun withdrawMeta(id: Int): @Meta {
        let Meta <- self.dictionaryOfMeta.remove(key: id) ?? panic("A resource does not exist at this id")
        return <- Meta
    }

    pub fun createMeta(id: Int, name: String): @Meta {
        return <- create Meta(_id: id, _name: name)
    }

    init() {
        self.dictionaryOfMeta <- {}
    }

}
</code></pre>
*Transactions*<br>
<pre><code>
// Deposit transaction
import Metadata from 0x01

transaction(id: Int, name: String) {

  prepare(acct: AuthAccount) {}

  execute {
    let Meta <- Metadata.createMeta(id: id, name: name)
    Metadata.depositMeta(Meta: <- Meta)

    log("Item deposited.")
  }
}
</code></pre>
<br>
<pre><code>
// Withdraw Transaction
import Metadata from 0x01

transaction(id: Int) {

  prepare(acct: AuthAccount) {}

  execute {
    let Meta <- Metadata.withdrawMeta(id: id)
    Metadata.depositMeta(Meta: <- Meta)

    log("Item withdrawn.")
  }
}
</code></pre>
<br>
2:<br>
*Scripts*<br>
<pre><code>
import Metadata from 0x01

pub fun main(id: Int): &Metadata.Meta{
  return Metadata.getReference(id: id)
}
</code></pre>
<br>
3:<br>
References are real good at letting you only work with some of the data without you having to load the whole resource.<br>

# Chapter 3 : Day 4
chapter 3 day 4

1: <i>Explain, in your own words, the 2 things resource interfaces can be used for (we went over both in today's content)</i><br>
The first thing you can use resource interfaces for is exposes data to a resource or struct.<br>
The second thing you can use resource interfaces for is exposes certain data to certain people.<br>

2: <i>Define your own contract. Make your own resource interface and a resource that implements the interface. Create 2 functions. In the 1st function, show an example of not restricting the type of the resource and accessing its content. In the 2nd function, show an example of restricting the type of the resource and NOT being able to access its content.</i><br>
# contract
![image](https://user-images.githubusercontent.com/12196769/174863294-5979289a-6f23-455d-bf20-f4b152fb1d02.png)<br>
# transaction
![image](https://user-images.githubusercontent.com/12196769/174863439-5bc8bdd7-b189-4811-b0d0-7f84bbc18583.png)<br>

3: <i>How would we fix this code?</i><br>
<pre>
  <code>
  pub contract Stuff {

    pub struct interface ITest {
      pub var greeting: String
      pub var favouriteFruit: String
    }

    // ERROR:
    // `structure Stuff.Test does not conform 
    // to structure interface Stuff.ITest`
    pub struct Test: ITest {
      pub var greeting: String
      pub var favoriteFruit: String   // add string varible favoriteFruit

      pub fun changeGreeting(newGreeting: String): String {
        self.greeting = newGreeting
        return self.greeting // returns the new greeting
      }

      init() {
        self.greeting = "Hello!"
      }
    }

    pub fun fixThis() {
      let test: @Test{ITest} <- Test()    // had to fix this 
      let newGreeting = test.changeGreeting(newGreeting: "Bonjour!") // ERROR HERE: `member of restricted type is not accessible: changeGreeting`
      log(newGreeting)
    }
}
  </code>
</pre>

# Chapter 3 : Day 5
<pre><code>
access(all) contract SomeContract {
    pub var testStruct: SomeStruct

    pub struct SomeStruct {

        //
        // 4 Variables
        //

        pub(set) var a: String

        pub var b: String

        access(contract) var c: String

        access(self) var d: String

        //
        // 3 Functions
        //

        pub fun publicFunc() {}

        access(contract) fun contractFunc() {}

        access(self) fun privateFunc() {}


        pub fun structFunc() {
            /**************/
            /*** AREA 1 ***/
            /**************/
            // read   - a, b, c, d
            // write  - a, b, c, d
        }

        init() {
            self.a = "a"
            self.b = "b"
            self.c = "c"
            self.d = "d"
        }
    }

    pub resource SomeResource {
        pub var e: Int

        pub fun resourceFunc() {
            /**************/
            /*** AREA 2 ***/
            /**************/
            // read   - a, b, c
            // write  - a, 
        }

        init() {
            self.e = 17
        }
    }

    pub fun createSomeResource(): @SomeResource {
        return <- create SomeResource()
    }

    pub fun questsAreFun() {
        /**************/
        /*** AREA 3 ****/
        /**************/
        // read   - a, b, c
        // write  - a
    }

    init() {
        self.testStruct = SomeStruct()
    }
}
</code></pre>
:Script:<br>
<pre><code>
import SomeContract from 0x01

pub fun main() {
  /**************/
  /*** AREA 4 ***/
  /**************/
  // read   - a, b
  // write  - a = yes but it want do anything so NO, 
}
</code></pre>
# Chapter 4 : Day 1
# Chapter 4 : Day 2
# Chapter 4 : Day 3
# Chapter 4 : Day 4
# Chapter 5 : Day 1
# Chapter 5 : Day 2
# Chapter 5 : Day 3
