#
# Copyright (C) 2024 Renesas Electronics Corporation.
# Copyright (C) 2024 EPAM Systems, Inc.
#
# SPDX-License-Identifier: Apache-2.0
#

# ######################################################################################################################
# Dependencies
# ######################################################################################################################

# gRPC lib
find_package(gRPC REQUIRED)

# Poco lib
find_package(Poco REQUIRED JSON DataSQLite Foundation)

# Systemd lib
find_package(PkgConfig REQUIRED)
pkg_check_modules(Systemd libsystemd REQUIRED)

# ######################################################################################################################
# Defines
# ######################################################################################################################

# ######################################################################################################################
# Includes
# ######################################################################################################################

include_directories(${AOS_CORE_COMMON_LIB_DIR}/include)

# ######################################################################################################################
# Modules
# ######################################################################################################################

add_subdirectory(logger)
add_subdirectory(migration)
add_subdirectory(utils)
add_subdirectory(iamclient)
