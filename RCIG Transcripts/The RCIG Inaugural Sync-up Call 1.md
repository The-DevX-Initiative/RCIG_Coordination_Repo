# The RCIG Inaugural Sync-up Call 1

## Common Themes That Came Out of Hacs Workshop

* People want higher assurances (constant time operation)

* Avoid branches when your code is goes through LLVM
 
* Fiat-Crypto is great getting Rust code up to speed is important because it may lead to no incentive to write code in Rust because it's going to look slower than C. 

* Getting a secret keyword in Rust or LLVM would be great.
    * Implementing a secret keyword in LLVM would tough in terms of maintainability
    * The secret keyword maybe considered a bit of niche for the for the hassle involved
    
* Diversity of tooling in Rust for high assurance gurantee's are maturing well. Having the tooling coalise into a community standard would be great.
 
* Tooling and observability of Async Runtimes is new to Rust but a great feature. Being able to inspect a lot of the stuff Rust let's you do

* Rust is gonna end up being as fast as C but with the added benefit of memory safety. We don't necessarily have to wait for commerical adoption if it's already fast with no possiblity of having stray pointers. 

## Getting Started with Cryptography in Rust: How is it and what can be improved? 

* There is no cryptography in the standard library, there are no exposed cryptography api's in the standard library
    * There is not straight up answer for someone coming in new to cryptography in Rust. 
    * A lot people are still reaching for Ring because it serves as a toolbox for Rust Crypto at the moment. 

* We need to address the lack of a toolbox for Rust Cryptography, this doesn't necessarily mean having crypto in the standard library, but the place where people go to get their Rust Crypto needs to be improved. 

* We want people to use pure Rust implementations so that they can get the maximum benefits of the Rust languages safety assurances and thats hard to find at the moment.

* We need a simple place for people to go and get a bootstrapped start that works for 90% of usecases then when people what to get deeper and do lower level cryptography there will be some recommeded implementations. 

* It could be said that there are more than groups of interested parties when it comes to Rust Cryptography (users & developers). There are a lot of different levels of users and developers. Crypto developers are not trying to build a stack of constructions all at once.

* It's possible that there should be as as many different levels of API as there are concepts regarding the Rust Crypto. Rust lends itself to this idea because if it's library first culture, in Rust you write your code where it's useful as a library. 

## Rust Cryptography & Web Assembly 

* Web Assembly support and no std support has improved a lot for cryptography libraries. 

* We need to see more Rust Cryptography being used in the browser. 

### What Role Do We Feel Wasm has in the Rust Cryptography Ecosystem? 

* Zero knowledge proof generation in the browser.

* The possibility of MPC (Multi Party Computation) in the browser.

* ARM working on a confidential compute enviroment and they are using Web Assembly inside a TEE. They are using Wasm to sandbox the user code.
    * Constant time behaviour is difficult when trying to do crypto in a Wasm sandbox.
    * Jitting and translation are probable causes for loss of constant time properties when doing Crypto in a Wasm sandbox, particularly with translation.


## Crate Curation for Rust Crypto

* We could create an Awesome Rust Cryptography list a comprehensive list of cryptography list of the ecosystem.

* Are we Crypto Yet. What's the difference between a Are We Crypto Yet vs an Awesome Rust Cryptography list. 


## A Vision Doc similar to Async but for Cryptography. 

* Vision doc is related to the ecosystem and not necessarily the language. 

* A vision doc should be ecosystem focused because there aren't the same language level deliverables in the same way as other parts of the ecosystem.

* Common Traits the we can use to interoperate. Interoperability is important but doesn't need to be in the standard library. A Vision could address the scope and frame of interoperability. 
    * Desiging good Traits are 10x harder than making a good implementation

* Golang has a blessed crypto library and aer careful with how they tinker with it. Rust Cryptography need to start crafting the directions that will lead people to find the right implementations for them, this could be in the form of lists. 


    