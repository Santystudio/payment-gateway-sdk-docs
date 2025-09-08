---
Title: Examples
Description: Real-world usage examples for the Payment Gateway SDK
---

# Integration Examples

This guide provides practical examples of how to use the Payment Gateway SDK in real-world applications. Each snippet is annotated to help developers understand the flow and logic behind each step.

---

## 💳 Example 1: Create a Payment

```js
import { createPayment } from 'payment-gateway-sdk';

const paymentData = {
  amount: 500,
  currency: 'USD',
  payment_method: 'card',
  customer_id: 'cus_123456'
};

createPayment(paymentData)
  .then(response => {
    console.log('Payment initiated:', response.payment_id);
    window.location.href = response.redirect_url;
  })
  .catch(error => {
    console.error('Payment failed:', error.message);
  });
import { verifyPayment } from 'payment-gateway-sdk';

const paymentId = 'pay_987654';

verifyPayment(paymentId)
  .then(status => {
    console.log('Payment status:', status);
  })
  .catch(error => {
    console.error('Verification failed:', error.message);
  });
import { refundPayment } from 'payment-gateway-sdk';

const refundData = {
  payment_id: 'pay_987654',
  reason: 'duplicate_transaction'
};

refundPayment(refundData)
  .then(response => {
    console.log('Refund processed:', response.refund_id);
  })
  .catch(error => {
    console.error('Refund failed:', error.message);
  });
try {
  const result = await createPayment(paymentData);
  console.log('Success:', result);
} catch (error) {
  if (error.code === 'AUTH_FAILED') {
    alert('Authentication error. Please check your API key.');
  } else {
    console.error('Unhandled error:', error);
  }
}
