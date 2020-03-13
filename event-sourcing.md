# Event Sourcing

All database transactions are writes to a database, a time series of events. In this model there are no read, update, or delete operations. The current value of any data entity -- for example, a customer -- is determined by aggregating all of the events associated with that entity. It would include an initial “Create Customer” event, followed by zero to many “Update Customer” events and zero or one “Delete Customer” event. This aggregation of events, known as a Materialized View, can be generated as events happen, as needed, or on a scheduled basis.

Because data and events are linked, they should include a version stamp. This is necessary when processing events over time as data formats change.

Event sourcing allows you to store an event in one place -- the Source of Truth for an entity -- and then propagate the event throughout your system as necessary. The events can also trigger multiple processes in your system while maintaining very loose coupling between processes.

By writing only events to a data store, several advantages are gained. They include:
Performance increases
Elimination of database locks
A data entity’s history is stored
Data does not need to exist in only one place
Events can be used to trigger loosely-coupled actions
