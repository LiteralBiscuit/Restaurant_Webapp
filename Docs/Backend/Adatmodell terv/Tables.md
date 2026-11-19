```
Users        {id, name, nickname?, email*, password_hash, phone*, address}
Staff        {id, name, username*, password_hash, role}
Categories   {id, name*}
Food_items   {id, category_id, name, description, img_path, price, is_available}
Orders       {id, user_id?, customer_name, phone, email, delivery_address,
              payment_method, created_at, status, estimated_time?, tracking_token*?, note?}
Order_items  {order_id, food_item_id, quantity}