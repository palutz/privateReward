# Private Reward

A privacy protecting system to allow all the contributors to freely support the projects they want, regardless of companies they work for, place where they live, ...


```mermaid
stateDiagram
    direction LR
    [*] --> User1
    User1 --> MergeRequest
    MergeRequest --> CreateTicket
    state Leo_Review {
      CreateTicket --> Vote
      direction RL
      Rev1 --> Vote
      Rev2 --> Vote
      Revn --> Vote
    }
    Vote --> Approved
    Vote --> Rejected
    state Leo_Reward {
      Approved --> Reward
      Reward --> User1Wallet
    }
    Approved --> Merged
```

## Create Ticket 
```
Ticket {
    Id : (ZKP?) Id of the User,
    MergeReq : URL with the hash of the Merge Reqeust,
    Wallet : wallet address for the reward
}
```

## LEO REVIEW

A voting system

## LEO REWARD

Simple Token 

## TODO

An overall system to orchestrate the review and the reward systems
