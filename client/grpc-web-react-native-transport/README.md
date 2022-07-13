# @alexeyproskuryakov/grpc-web-react-native-transport
Transport for use with [@alexeyproskuryakov/grpc-web](https://github.com/alexeyproskuryakov/grpc-web)
that works with React Native.

## Usage
When making a gRPC request, specify this transport:

```typescript
import { grpc } from '@alexeyproskuryakov/grpc-web';
import { ReactNativeTransport } from '@alexeyproskuryakov/grpc-web-react-native-transport';

grpc.invoke(MyService.DoQuery, {
  host: "https://example.com",
  transport: ReactNativeTransport(),
  /* ... */
})
```

Alternatively specify the Default Transport when your server/application bootstraps:
```typescript
import { grpc } from '@alexeyproskuryakov/grpc-web';
import { ReactNativeTransport } from '@alexeyproskuryakov/grpc-web-react-native-transport';

// Do this first, before you make any grpc requests!
grpc.setDefaultTransport(ReactNativeTransport());
```
