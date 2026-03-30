# Dispute Deadline Implementation TODO

## Steps:
- [x] 1. Update Escrow entity to add `disputeDeadline` field
- [x] 2. Create and apply new TypeORM migration for `disputeDeadline` column
- [x] 3. Update `escrow.service.ts`: set deadline in `fileDispute()`, implement `triggerDefaultResolution()`
- [x] 4. Add endpoint in `escrow.controller.ts` for `/dispute/default-resolve`
- [x] 5. Add cron job in `escrow-scheduler.service.ts` to check overdue disputes every 5 min
- [ ] 6. Update tests and verify
- [ ] 7. Run migration and test end-to-end

**Completed:** Steps 1-5
**Next:** Step 6 - tests/migration
