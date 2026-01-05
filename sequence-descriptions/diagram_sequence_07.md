# Sequence Diagram Description: Shipment Management

**Diagram File**: `diagram_sequence_07.jpg`

## 1. Use Case Name
**Shipper: Manage Shipments**

## 2. Actors Involved
- **Shipper**: Logistics provider/user.
- **UI** (Shipment Panel).
- **System**.
- **Shipment Service**.
- **Database**.

## 3. Pre-conditions
- Shipper account exists in the database.

## 4. Post-conditions
- Shipper is authenticated.
- Shipment status is updated (e.g., "Delivered").

## 5. Step-by-Step Interaction Flow

### Scenario A: Shipper Login
1.  **Shipper** logs in.
2.  **System** authenticates against **Database**.
3.  **UI** grants access to Shipment Panel.

### Scenario B: View/Update Shipment
1.  **Shipper** views shipment info.
2.  **System** -> **Shipment Service** -> **Database** fetches details.
3.  **Shipper** updates status (e.g., to "In Transit").
4.  **System** saves update to **Database**.
5.  **UI** confirms "Status Updated".

## 6. System Behavior Explanation
Extends the system's functionality to logistics. It introduces a specialized **Shipment Service** to handle tracking and status updates, separate from the core order logic.

## 7. Conclusion
Completes the order lifecycle by allowing external actors (Shippers) to manage the delivery phase.
