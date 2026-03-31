# Ρύθμιση branch protection για το `main`

Αυτά τα βήματα τα κάνει ο repo admin στο GitHub:

1. Άνοιξε: `Settings` -> `Branches` -> `Add branch protection rule`.
2. Στο **Branch name pattern** βάλε: `main`.
3. Ενεργοποίησε:
   - **Require a pull request before merging**
   - **Require approvals**: `1` (ή περισσότερα αν θέλετε)
   - **Dismiss stale pull request approvals when new commits are pushed**
   - **Require status checks to pass before merging**
4. Στα status checks πρόσθεσε το check του workflow:
   - `python-checks`
5. Ενεργοποίησε:
   - **Require conversation resolution before merging**
   - **Do not allow bypassing the above settings** (όπου είναι διαθέσιμο)
6. Αποθήκευσε τη ρύθμιση.

## Προτεινόμενες επιπλέον ρυθμίσεις

- Κλείδωμα direct push στο `main`.
- Περιορισμός force pushes στο `main`.
- Αν υπάρχει ομάδα reviewers, χρησιμοποίησε CODEOWNERS για αυτόματη ανάθεση.
