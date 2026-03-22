
Supply Chain Streaming Pipeline Instructions
1. Upload Source Data
text
FileStore/
└── streaming_input/
    ├── shipment_events_1.json  (paste JSON from earlier)
    └── shipment_events_2.json  (new events)
2. Run Streaming Pipeline
python
# Copy-paste the complete streaming code from previous response
# Cell 1: Imports + schema + raw_stream
# Cell 2: processed_stream transformations  
# Cell 3: query = writeStream... + query.awaitTermination()
3. Verify Output
sql
-- Auto-created table
SELECT * FROM supply_chain_metrics;

-- Schema & stats
DESCRIBE supply_chain_metrics;


📈 Expected Output
text
warehouse_id | event_date  | status    | shipment_count
WH1         | 2026-03-21 | shipped   | 2
WH1         | 2026-03-21 | delivered | 1