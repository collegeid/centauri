# Centauri App - One Week Project

## Preview
[Link to Notebook]([https://nbviewer.jupyter.org/url/path/to/your/notebook.ipynb](https://notebooks.githubusercontent.com/view/ipynb?browser=firefox&bypass_fastly=true&color_mode=auto&commit=d189790f89ddd1cb0f9615955ec53404b1221f99&device=unknown_device&docs_host=https%3A%2F%2Fdocs.github.com&enc_url=68747470733a2f2f7261772e67697468756275736572636f6e74656e742e636f6d2f636f6c6c65676569642f63656e74617572692f643138393739306638396464643163623066393631353935356563353334303462313232316639392f43656e74617572695f417070735f4f6e655f5765656b5f50726f6a6563742e6970796e62&logged_in=true&nwo=collegeid%2Fcentauri&path=Centauri_Apps_One_Week_Project.ipynb&platform=linux&repository_id=807648343&repository_type=Repository&version=126#7b5783be-4864-40ce-90bc-d65dea69ff2f))

## Features of Electronic Equipment Borrowing System:

1. **Software Name Initialization**
   - This feature allows users to initialize the software name when running the system for the first time.

2. **Member Registration**
   - This feature allows users to register as members by providing information such as name, address, phone number, username, and password.

3. **Login**
   - Users can log into the system using the username and password they have registered.

4. **Search and List Electronic Equipment**
   - Users can search for electronic equipment based on specific categories and view a list of equipment that matches the search criteria.

5. **Borrow Electronic Equipment**
   - This feature allows users to borrow electronic equipment available in the system.
   - `Admin, staff` can make borrowing requests for users.

6. **Return Electronic Equipment**
   - Users can return electronic equipment that has been borrowed previously.

7. **Electronic Equipment Availability Status**
   - This feature allows users to see the availability status of electronic equipment, whether the equipment is available for borrowing or is currently borrowed by another user.

8. **Borrowing History**
   - Users can view the borrowing history of electronic equipment, both personally.
   - `Admin, staff` can view user history based on `nama` and the entire History List from various Users.

9. **Electronic Equipment Data Management**
   - Admin has access to add, delete, or modify electronic equipment data in the system.

10. **Account Management**
    - Admin can manage user accounts, including adding, deleting, modifying, or viewing account profiles.

11. **Logout**
    - Users can log out of their login session.

12. **Exit**
    - Users can exit the system altogether.
    - 
## Function Explanations:

### Initialization
   - Initializes the software name based on user input.

### Data Storage (List Tuple)
   - Stores variables `anggota` for admin, staff, and user profiles tied to their respective accounts.
   - Stores borrowing data in the list `riwayat_peminjaman` made by users.

### Member Registration 

- Function for registering users to create a profile
- Creates a user account connected to the user profile

Parameter Specifications
- A. Profile
   1. Name `(String)`
   2. Address `(String)`
   3. Phone Number `(Integer)`
   4. NIK (National Identification Number) `(Integer)`

- B. Account
   1. Username `(String)`
   2. Password `(String)`

#### Note: `append()`
   - Inserts an element into the Tuple List used as a template with reference to the variable named `anggota`.

### Verification

- Function for accessing Centauri Apps
- Multi-level login detection (visitor, staff, or admin)

#### Explanation of variable `check`, and function `next()`

   - `check` will iterate through the variable `anggota` and the result of the check will be referred to as `akun`. It then checks if there are values from the input `username` and `password` that match/are registered. If the result is positive, it will return a default value of `True`, but if not, it will return output as `None` or `false` and print that the `account is not registered`.

   - The function `next()` is used to return the `iterator` value, in this case, it is `akun` that we use as an `iterator`. Each cluster of iterations is separated by `{}` as `one cluster of iterators in the list`.
   - 
#### Tool List 
  - Searching for tools based on Name or Description
  - Displaying a List of Tools according to the Search
  - Showing `Nomor Inventaris, Nama, deskripsi`, and `status` of the searched items

#### Borrowing Equipment by Admin/Staff()
 - Admin/Staff Enter Inventory Number and Borrower's Name
 - Borrowing is done based on the `Nomor Inventaris Barang`
 - check the status of the item whether it is `tersedia` or currently `dipinjam`
 - record who the borrower is, the borrowing date with a maximum return period of 7 days
   
#### Borrow Equipment
 - User Side
 - Borrowing is done based on the `Nomor Inventaris Barang`
 - check the status of the item whether it is `tersedia` or currently `dipinjam`
 - record who the borrower is (in this case, visitor's account), the borrowing date with a maximum return period of 7 days

#### Return Equipment
- Returning equipment based on inventory number
- Calculate the late fee per day which is 10,000 rupiah

#### Track Equipment
- Tracking an Equipment based on `Nomor Inventaris`, and show it's `Sisa Waktu Peminjaman`

#### History

 - borrowing history with `level akses admin`
 - view personal borrowing `level admin`
 - borrowing of all members, by searching for members based on `nama`
 - If the level is `pengunjung`, it will display borrowed items based on the account owner currently in use

#### Equipment Management
 - admin level management access to add a projector with parameters `nama_alat, deksripsi, nomor_inventaris`
 - delete projector based on `nomor_inventaris`
 - change equipment information based on `nomor_inventaris`

#### Account Management
 - add `profil` and `akun`
 - delete `akun` based on `username`
 - modify `akun` based on `username`
 - view `akun` based on `username`

#### main()

- Initialize `software_name`
- Display Main Page
  - Login
  - Register
  - Exit

- Visitor
   1. Search and List Electronic Equipment
   2. Electronic Equipment Availability Status
   3. Borrowing History (Personal Account)
   4. Logout
   5. Exit


- Staff
  1. Search and List Electronic Equipment
  2. Borrow Electronic Equipment (For Visitors)
  3. Return Electronic Equipment
  4. Electronic Equipment Availability Status
  5. Borrowing History (Search History by User Name)
  6. Logout
  7. Exit

- Admin
  1. Search and List Electronic Equipment
  2. Borrow Electronic Equipment (For Visitors)
  3. Return Electronic Equipment
  4. Electronic Equipment Availability Status
  5. Borrowing History (Search History by User)
  6. Electronic Equipment Data Management
  7. Account Management
  8. Logout
  9. Exit

<hr>

## By Centauri - 29, May 2024 (febrian.id)
