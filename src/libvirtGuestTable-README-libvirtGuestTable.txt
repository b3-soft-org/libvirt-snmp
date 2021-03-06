************************************************************************
libvirtGuestTable README
------------------------------------------------------------------------
  This readme file describes the code generated by mib2c (using the MIBs
  for Dummies (MFD) configuration file). The code generated was
  generated specifically for the following SNMP table:

     libvirtGuestTable

  Your code will be called when the snmp agent receives requests for
  the libvirtGuestTable table.  The agent will start by looking for the right
  row in your existing data to operate on, if one exists.


  Configuration Variables
  ------------------------------------------------------------
  Some variables used for code generation may be set to affect the code
  generation. You may override these variables by setting them in the
  file defaults/table-libvirtGuestTable.m2d, and then re-running mib2c.

    m2c_table_settable (currently '1')
    --------------------------------------------------------
    This variable determines whether or not code is generated to support
    MIB object which have an access of read-write or read-create. The
    default is set based on whether or not the table contains writable
    objects, but can be over-ridden.

    Syntax: @eval $m2c_table_settable = 0@


    m2c_table_dependencies (currently '0')
    --------------------------------------------------------
    This variable determines whether or not code is generated to support
    checking dependencies between columns, rows or tables. The default
    is set based on whether or not the table contains writable objects,
    but can be over-ridden.

    Syntax: @eval $m2c_table_dependencies = 0@


    m2c_table_row_creation (currently '1')
    --------------------------------------------------------
    This variable determines whether or not code is generated to support
    checking creation of new rows via SNMP. The default is set based on
    whether or not the table contains read-create objects, but can be
    over-ridden.

    Syntax: @eval $m2c_table_row_creation = 0@


    m2c_context_reg (currently 'netsnmp_data_list')
    --------------------------------------------------------
    This variable contains the structure name to typedef for the
    libvirtGuestTable_registration.

    During initilization, you will provide a pointer to a structure of
    this type. This pointer is used as a parameter to many functions so
    that you have access to your registration data. The default is a
    netsnmp_data_list pointer, which will allow you to keep multiple
    pointers tagged by a text name. If you have a new or existing structure
    you would rather use, you can redefine this variable.


    To avoid regenerating code, you may also change this typedef directly
    in the libvirtGuestTable.h header.

    Syntax: @eval $m2c_context_reg = "struct my_registration_context@


    m2c_data_context (currently 'generated')
    --------------------------------------------------------
    This variable contains the structure name to typedef for the
    libvirtGuestTable_data.

    This typedef is used in the row request context structure for the table,
    libvirtGuestTable_rowreq_ctx.

    The typedef in the primary table context will be used for the data and
    undo structure types. This structure should contain all the data
    needed for all the columns in the table. The default is 'generated',
    which will cuase a new data strcuture to be generated with data members
    for each column.

    To avoid regenerating code, you may also change this typedef directly
    in the libvirtGuestTable.h header.

    Syntax: @eval $m2c_data_context = "struct my_data_context"@


    m2c_data_allocate (currently '0')
    --------------------------------------------------------
    This variable determines whether or not the data context (see above)
    requires memory to be allocated. The default generated data structure
    does not. If you are using a custom data context which needs to
    allocate memory, override this value and two additional functions
    will be generated:

      libvirtGuestTable_allocate_data
      libvirtGuestTable_release_data

    Syntax: @eval $m2c_data_allocate = 1@


    m2c_data_init (currently '1')
    --------------------------------------------------------
    This variable determines whether or not the data context (see above)
    or any other items you have added to the table context requires
    initialization. The default generated data structure does not. If you
    are using a custom data context or have added items needing initialization
    to the table context, override this value and two additional functions
    will be generated:

      libvirtGuestTable_rowreq_ctx_init
      libvirtGuestTable_rowreq_ctx_cleanup

    Syntax: @eval 1 = 1@


    m2c_table_access (currently 'container-cached')
    ------------------------------------------------------------------
    This variable determines which data interface will be use to generate
    code for looking up data for a given index. The default is the
    'container-cached' access code, which caches the data in a netsnmp-
    container (usually a sorted array).

    Available options can be determined by checking for mib2c configuration
    files that begin with 'mfd-access-*'.

    Syntax: @eval $m2c_table_access = 'container-cached'@


    m2c_include_examples (currently '1')
    ------------------------------------------------------------------
    This variable determines whether or not to generate example code. The
    default is to generate example code.

    Syntax: @eval $m2c_include_examples = 0@


    m2c_data_transient (currently '0')
    ------------------------------------------------------------------
    This variable determines how the generated example code deals with the
    data during data lookup. See the table readme file for details on how
    the current table access method interprets this value. In general,
    a value of 0 indicates persistent data, 1 indicates semi-transient and
    2 indicates transient data.

    Syntax: @eval $m2c_data_transient = 0@


 Index(es) for the libvirtGuestTable table
  ------------------------------------------------------------
  The index(es) for the libvirtGuestTable table are:

     libvirtGuestUUID:
        Syntax:      UUID
        DataType:    OCTETSTR
        ASN type:    ASN_OCTET_STR
        C-code type: char

  You should know how to set all these values from your data context,
  libvirtGuestTable_data.


************************************************************************
libvirtGuestTable File Overview
------------------------------------------------------------------------
  Several files have been generated to implement the libvirtGuestTable
  table. We'll go through these files, one by one, explaining each and
  letting you know which you need to edit.


File: libvirtGuestTable_data_access.[c|h]
------------------------------------------------------------------------
  The libvirtGuestTable_data_access file contains the interface to your data in
  its raw format.  These functions are used to build the row cache or
  locate the row (depending on the table access method).

  Set MIB context
  -----------------
  TODO : Set MIB index values
  FUNC : libvirtGuestTable_indexes_set
  WHERE: libvirtGuestTable_data_access.c

  This is a convenience function for setting the index context from
  the native C data. Where necessary, value mapping should be done.

  This function should update the table index values (found in
  tbl_idx) for the given raw data.


  container summary
  ------------------------
    The container data access code is for cases when you want to
    store your data in the agent/sub-agent.

    ... to be continued...


  cache summary
  ------------------------
    The container-cached data access code is for cases when you want to
    cache your data in the agent/sub-agent.

    ... to be continued...




File: libvirtGuestTable_enums.h
------------------------------------------------------------------------
  This file contains macros for mapping enumeration values when the
  enumerated values defined by the MIB do not match the values used
  internally.

  Review this file to see if any values need to be updated.


File: libvirtGuestTable_data_get.c
------------------------------------------------------------------------
  Get data for column
  -------------------
  TODO : retrieve column data from raw data
  FUNC : libvirtGuestName_get

  Get data for column
  -------------------
  TODO : retrieve column data from raw data
  FUNC : libvirtGuestState_get

  Get data for column
  -------------------
  TODO : retrieve column data from raw data
  FUNC : libvirtGuestCpuCount_get

  Get data for column
  -------------------
  TODO : retrieve column data from raw data
  FUNC : libvirtGuestMemoryCurrent_get

  Get data for column
  -------------------
  TODO : retrieve column data from raw data
  FUNC : libvirtGuestMemoryLimit_get

  Get data for column
  -------------------
  TODO : retrieve column data from raw data
  FUNC : libvirtGuestCpuTime_get

  Get data for column
  -------------------
  TODO : retrieve column data from raw data
  FUNC : libvirtGuestRowStatus_get



File: libvirtGuestTable_data_set.c
------------------------------------------------------------------------

  This code was generated based on the following assumptions or settings:

  1) Some of the values for this table have DEPENDENCIES on other objects.

  DEPENDENCIES on other objects complicates SET request processing. When
  one or more columns in a table depend on another object (in the same
  table, or in another table), a DEPENDENCY exists. For example, if you
  have a table that determine a color with three columns (red, green and
  blue) that define the percentage of each primary color, the total for
  the three columns must equal 100 percent. So, in addition to checking
  that each colums has a valid value between 0 and 100, the total of
  all three columns must equal 100.

  Set $m2c_table_dependencies = 0 in defaults/table-libvirtGuestTable.m2d
  and regenerate code if this assumption is incorrect.

  2) This table supports ROW CREATION.

  Supporting ROW CREATION allows new rows to be created via SNMP requests.

  To support row creation, the index component of an incoming set request must
  be validated. A funciton is generated for each individual index component,
  and another for validating all the index components together.


  Validate index component
  ------------------------
  TODO : validate the specified index component
  FUNC : libvirtGuestUUID_check_index


  Validate index
  --------------
  TODO : check that all index components are valid
  FUNC : libvirtGuestTable_validate_index



  Undo setup
  ----------
  TODO : save data for undo
  FUNC : libvirtGuestTable_undo_setup

  This function will be called before the individual undo_setup functions are
  called. This is where you should save any undo information which is not
  directly related to a particular column. This function will only be called
  once per row. After this function is called, any column which is being
  set will have its individual node undo_setup function called.



  Check value for column
  ----------------------
  TODO : perform additional validations on values for a set request
  FUNC : libvirtGuestState_check_value

  The generated code will automatically validate incoming requests against
  all the requirements specified by the syntax of the MIB. However, it is
  often the case that additional requirements are specified in the
  description of a MIB object. Those type of validations should be checked
  in this function.


  Undo setup for column
  ---------------------
  TODO : save the value for column
  FUNC : libvirtGuestState_undo_setup

  After the table level undo setup function has been called, the individual
  node undo setup functions will be called for columns which are being set.


  Set value for column
  --------------------
  TODO : set the value for column
  FUNC : libvirtGuestState_set

  After all the validations have been passed, this function will be called to
  set the new value.


  Undo value for column
  ---------------------
  TODO : undo set for column
  FUNC : libvirtGuestState_undo

  If an error occurs after a column has been set, this function will be called
  to undo the set and restore the previous state.

  Check value for column
  ----------------------
  TODO : perform additional validations on values for a set request
  FUNC : libvirtGuestRowStatus_check_value

  The generated code will automatically validate incoming requests against
  all the requirements specified by the syntax of the MIB. However, it is
  often the case that additional requirements are specified in the
  description of a MIB object. Those type of validations should be checked
  in this function.


  Undo setup for column
  ---------------------
  TODO : save the value for column
  FUNC : libvirtGuestRowStatus_undo_setup

  After the table level undo setup function has been called, the individual
  node undo setup functions will be called for columns which are being set.


  Set value for column
  --------------------
  TODO : set the value for column
  FUNC : libvirtGuestRowStatus_set

  After all the validations have been passed, this function will be called to
  set the new value.


  Undo value for column
  ---------------------
  TODO : undo set for column
  FUNC : libvirtGuestRowStatus_undo

  If an error occurs after a column has been set, this function will be called
  to undo the set and restore the previous state.



  Commit changes
  --------------
  TODO : commit changes
  FUNC : libvirtGuestTable_commit

  After all values have been set, the commit function will be called.





************************************************************************
libvirtGuestTable Reference
------------------------------------------------------------------------

Function flow
----------------------------------------------------
To give you the general idea of how the functions flow works, this
example flow is from a complete table implementation.

NOTE: Depending on your configuration, some of the functions used in the
      examples below  may not have been generated for the
      libvirtGuestTable table.

      Conversely, the examples below may not include some functions that
      were generated for the libvirtGuestTable table.

To watch the flow of the libvirtGuestTable table, use the
following debug tokens:

        snmp_agent
        helper:table:req
        libvirtGuestTable
        verbose:libvirtGuestTable
        internal:libvirtGuestTable

e.g.
        snmpd -f -Le -DlibvirtGuestTable,verbose:libvirtGuestTable,internal:libvirtGuestTable


Initialization
--------------------------------
init_xxxTable: called                           xxx.c
   initialize_table_xxxTable                    xxx.c
      _xxxTable_initialize_interface            xxx_interface.c
         xxxTable_init_data                     xxx_data_access.c
      _xxxTable_container_init                  xxx_interface.c
         xxxTable_container_init                xxx_data_access.c


GET Request
--------------------------------
_cache_load                                     xxx_interface.c
   xxxTable_cache_load                          xxx_data_access.c
      xxxTable_allocate_rowreq_ctx              xxx_interface.c
         xxxTable_allocate_data                 xxx_data_get.c
         xxxTable_rowreq_ctx_init               xxx_data_get.c
      xxxTable_indexes_set                      xxx_data_get.c
         xxxTable_indexes_set_tbl_idx           xxx_data_get.c

xxxTable_pre_request

_mfd_xxxTable_object_lookup                     xxx_interface.c
   xxxTable_row_prep                            xxx_data_access.c

_mfd_xxxTable_get_values                        xxx_interface.c
   _mfd_xxxTable_get_column                     xxx_interface.c
      yyy_get                                   xxx_data_get.c

xxxTable_post_request


GETNEXT Request
--------------------------------
_cache_load                                     ...
xxxTable_pre_request                            ...
_mfd_xxxTable_object_lookup                     ...
_mfd_xxxTable_get_values                        ...
xxxTable_post_request                           ...


SET Request: success
--------------------------------
_cache_load                                     ...
xxxTable_pre_request
_mfd_xxxTable_object_lookup                     ...

_mfd_xxxTable_check_objects                     xxx_interface.c
   _xxxTable_check_column                       xxx_interface.c
      yyy_check_value                           xxx_data_set.c

_mfd_xxxTable_undo_setup                        xxx_interface.c
   xxxTable_allocate_data                       ...
   xxxTable_undo_setup                          xxx_interface.c
      _xxxTable_undo_setup_column               xxx_interface.c
         yyy_undo_setup                         xxx_data_set.c

_mfd_xxxTable_set_values                        xxx_interface.c
   _xxxTable_set_column                         xxx_interface.c
      yyy_set                                   xxx_data_set.c

_mfd_xxxTable_check_dependencies                xxx_interface.c
   xxxTable_check_dependencies                  xxx_data_set.c

_mfd_xxxTable_commit                            xxx_interface.c
   xxxTable_commit                              xxx_data_set.c

_mfd_xxxTable_undo_cleanup                      xxx_interface.c
   xxxTable_undo_cleanup                        xxx_data_set.c
      xxxTable_release_data                     ...

xxxTable_post_request                           ...


SET Request: row creation
--------------------------------
_cache_load                                     ...
xxxTable_pre_request

_mfd_xxxTable_object_lookup                     ...
   xxxTable_index_from_oid                      xxx_interface.c
   xxxTable_allocate_rowreq_ctx                 ...
      ...
   _xxxTable_check_indexes                      xxx_interface.c
      yyy_check_index                           xxx_data_set.c
      xxxTable_validate_index                   xxx_data_set.c

_mfd_xxxTable_check_objects                     ...
   _xxxTable_check_column                       ...
      yyy_check_value                           ...
   _xxxTable_check_column                       ...
      yyy_check_value                           ...

_mfd_xxxTable_undo_setup                        ...
_mfd_xxxTable_set_values                        ...
_mfd_xxxTable_check_dependencies                ...
_mfd_xxxTable_commit                            ...
_mfd_xxxTable_undo_cleanup                      ...
xxxTable_post_request                           ...


SET Resuest: value error
--------------------------------
_cache_load                                     ...
xxxTable_pre_request                            ...
_mfd_xxxTable_object_lookup                     ...

_mfd_xxxTable_check_objects                     ...
   _xxxTable_check_column                       ...
      yyy_check_value                           ...
      ERROR:"yyy value not supported"

xxxTable_post_request                           ...


SET Request: commit failure
--------------------------------
_cache_load                                     ...
xxxTable_pre_request                            ...
_mfd_xxxTable_object_lookup                     ...
_mfd_xxxTable_check_objects                     ...
_mfd_xxxTable_undo_setup                        ...
_mfd_xxxTable_set_values                        ...
_mfd_xxxTable_check_dependencies                ...

_mfd_xxxTable_commit                            ...
   xxxTable_commit                              ...
   ERROR: bad rc -1

_mfd_xxxTable_undo_commit                       xxx_interface.c
   xxxTable_undo_commit                         xxx_data_set.c

_mfd_xxxTable_undo_values                       xxx_interface.c
   _xxxTable_undo_column                        xxx_interface.c
      yyy_undo                                  xxx_data_set.c

_mfd_xxxTable_undo_cleanup                      ...
xxxTable_post_request                           ...


Row release (user initiated)
--------------------------------
xxxTable_release_rowreq_ctx                     xxx_interface.c
   xxxTable_rowreq_ctx_cleanup                  xxx_data_get.c
   xxxTable_release_data                        xxx_data_get.c



Table / column details
----------------------------------------------------
/**********************************************************************
 **********************************************************************
 ***
 *** Table libvirtGuestTable
 ***
 **********************************************************************
 **********************************************************************/
/*
 * LIBVIRT-MIB::libvirtGuestTable is subid 1 of libvirtObjects.
 * Its status is Current.
 * OID: .1.3.6.1.4.1.12345.1.1, length: 9
*/

/*---------------------------------------------------------------------
 * LIBVIRT-MIB::libvirtGuestEntry.libvirtGuestUUID
 * libvirtGuestUUID is subid 1 of libvirtGuestEntry.
 * Its status is Current, and its access level is NoAccess.
 * OID: .1.3.6.1.4.1.12345.1.1.1.1
 * Description:
The UUID of the virtual guest.
 *
 * Attributes:
 *   accessible 0     isscalar 0     enums  0      hasdefval 0
 *   readable   0     iscolumn 1     ranges 1      hashint   1
 *   settable   0
 *   hint: 4x-2x-2x-2x-6x
 *
 * Ranges:  16;
 *
 * Its syntax is UUID (based on perltype OCTETSTR)
 * The net-snmp type is ASN_OCTET_STR. The C type decl is char (char)
 * This data type requires a length.  (Max 16)
 *
 *
 *
 * NOTE: NODE libvirtGuestUUID IS NOT ACCESSIBLE
 *
 *
 */
/*---------------------------------------------------------------------
 * LIBVIRT-MIB::libvirtGuestEntry.libvirtGuestName
 * libvirtGuestName is subid 2 of libvirtGuestEntry.
 * Its status is Current, and its access level is ReadOnly.
 * OID: .1.3.6.1.4.1.12345.1.1.1.2
 * Description:
Name of active virtual guest.
 *
 * Attributes:
 *   accessible 1     isscalar 0     enums  0      hasdefval 0
 *   readable   1     iscolumn 1     ranges 0      hashint   0
 *   settable   0
 *
 *
 * Its syntax is OCTETSTR (based on perltype OCTETSTR)
 * The net-snmp type is ASN_OCTET_STR. The C type decl is char (char)
 * This data type requires a length.
 */
/*---------------------------------------------------------------------
 * LIBVIRT-MIB::libvirtGuestEntry.libvirtGuestState
 * libvirtGuestState is subid 3 of libvirtGuestEntry.
 * Its status is Current, and its access level is Create.
 * OID: .1.3.6.1.4.1.12345.1.1.1.3
 * Description:
Current state of the active guest.
 *
 * Attributes:
 *   accessible 1     isscalar 0     enums  1      hasdefval 0
 *   readable   1     iscolumn 1     ranges 0      hashint   0
 *   settable   1
 *
 * Enum range: 4/8. Values:  running(1), blocked(2), paused(3), shutdown(4), shutoff(5), crashed(6)
 *
 * Its syntax is INTEGER (based on perltype INTEGER)
 * The net-snmp type is ASN_INTEGER. The C type decl is long (u_long)
 */
/*---------------------------------------------------------------------
 * LIBVIRT-MIB::libvirtGuestEntry.libvirtGuestCpuCount
 * libvirtGuestCpuCount is subid 4 of libvirtGuestEntry.
 * Its status is Current, and its access level is ReadOnly.
 * OID: .1.3.6.1.4.1.12345.1.1.1.4
 * Description:
Number of virtual CPUs the virtual guest uses.
 *
 * Attributes:
 *   accessible 1     isscalar 0     enums  0      hasdefval 0
 *   readable   1     iscolumn 1     ranges 1      hashint   0
 *   settable   0
 *
 * Ranges:  0 - 65535;
 *
 * Its syntax is UNSIGNED32 (based on perltype UNSIGNED32)
 * The net-snmp type is ASN_UNSIGNED. The C type decl is u_long (u_long)
 */
/*---------------------------------------------------------------------
 * LIBVIRT-MIB::libvirtGuestEntry.libvirtGuestMemoryCurrent
 * libvirtGuestMemoryCurrent is subid 5 of libvirtGuestEntry.
 * Its status is Current, and its access level is ReadOnly.
 * OID: .1.3.6.1.4.1.12345.1.1.1.5
 * Description:
Current amount of memory (in MiB) used by the virtual guest.
 *
 * Attributes:
 *   accessible 1     isscalar 0     enums  0      hasdefval 0
 *   readable   1     iscolumn 1     ranges 1      hashint   0
 *   settable   0
 *
 * Ranges:  0 - -1;
 *
 * Its syntax is GAUGE (based on perltype GAUGE)
 * The net-snmp type is ASN_GAUGE. The C type decl is u_long (u_long)
 */
/*---------------------------------------------------------------------
 * LIBVIRT-MIB::libvirtGuestEntry.libvirtGuestMemoryLimit
 * libvirtGuestMemoryLimit is subid 6 of libvirtGuestEntry.
 * Its status is Current, and its access level is ReadOnly.
 * OID: .1.3.6.1.4.1.12345.1.1.1.6
 * Description:
The maximum amount of memory (in MiB) that can be used by the virtual
	guest.
 *
 * Attributes:
 *   accessible 1     isscalar 0     enums  0      hasdefval 0
 *   readable   1     iscolumn 1     ranges 1      hashint   0
 *   settable   0
 *
 * Ranges:  0 - -1;
 *
 * Its syntax is UNSIGNED32 (based on perltype UNSIGNED32)
 * The net-snmp type is ASN_UNSIGNED. The C type decl is u_long (u_long)
 */
/*---------------------------------------------------------------------
 * LIBVIRT-MIB::libvirtGuestEntry.libvirtGuestCpuTime
 * libvirtGuestCpuTime is subid 7 of libvirtGuestEntry.
 * Its status is Current, and its access level is ReadOnly.
 * OID: .1.3.6.1.4.1.12345.1.1.1.7
 * Description:
The CPU time used by the virtual guest, in nanoseconds.
 *
 * Attributes:
 *   accessible 1     isscalar 0     enums  0      hasdefval 0
 *   readable   1     iscolumn 1     ranges 0      hashint   0
 *   settable   0
 *
 *
 * Its syntax is COUNTER64 (based on perltype COUNTER64)
 * The net-snmp type is ASN_COUNTER64. The C type decl is U64 (U64)
 */
/*---------------------------------------------------------------------
 * LIBVIRT-MIB::libvirtGuestEntry.libvirtGuestRowStatus
 * libvirtGuestRowStatus is subid 9 of libvirtGuestEntry.
 * Its status is Current, and its access level is Create.
 * OID: .1.3.6.1.4.1.12345.1.1.1.9
 * Description:
Status of the virtual guest.

	 A new virtual guest can be activated when either libvirtGuestName or
	 libvirtGuestUUID is specified and libvirtGuestState is either set to
	 running or paused.

	 A virtual guest can be destroyed by setting this column value to
	 'destroy'.

 *
 * Attributes:
 *   accessible 1     isscalar 0     enums  1      hasdefval 0
 *   readable   1     iscolumn 1     ranges 0      hashint   0
 *   settable   1
 *
 * Enum range: 3/8. Values:  active(1), notInService(2), notReady(3), createAndGo(4), createAndWait(5), destroy(6)
 *
 * Its syntax is RowStatus (based on perltype INTEGER)
 * The net-snmp type is ASN_INTEGER. The C type decl is long (u_long)
 */


