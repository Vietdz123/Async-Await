# Concurrency In SwiftUI


`Task` trong swift là 1 `asynchronous operation`, nó cung cấp cho ta giải pháp thay thế cho `DispatchQueue.main.async {}`. 

```swift
func newConcurrencyCode() {
    Task {
        // Executes asynchronously on the main thread
        // Depending on whether the newConcurrencyCode function
        // is implemented by an object protected by MainActor previously
    }
    
    Task { @MainActor in
        // Executes asynchronously on the main thread
        // explicitly
    }
    
    Task(priority: .background) {
        // Executes asynchronously on any thread
        // with background priority
    }
}
```


# I. Async await

`Async/Await` là 1 feature của Swift được sử dụng cho việc handle concurrency code. `async` được sử dụng để chỉ định rằng 1 `func` hoặc 1 `computed property` sẽ return lại 1 kết quả không đồng bộ, trong khi đó `await` được sử dụng để đợi kết quả `async` đó khi gọi 1 functions asynchronous.

![]()


# V. Reference

1. [Swift Concurrency](https://onnerb.medium.com/swift-concurrency-fd42c072234e)